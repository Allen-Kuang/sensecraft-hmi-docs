# 🔒 安全配置指南

本文档说明了项目部署的安全配置和最佳实践。

## 🛡️ API Token 安全

### 最小权限原则

创建 Cloudflare API Token 时，请遵循最小权限原则：

#### 推荐的 Token 配置
```
Token name: GitHub Actions - Pages Deploy (sensecraft-hmi-docs)

Permissions:
✅ Account: Cloudflare Pages:Edit
❌ Zone: Zone:Read (仅当需要自定义域名时)
❌ Zone: Zone Settings:Read (仅当需要自定义域名时)

Account Resources:
✅ Include: Specific account (选择您的账户)

Zone Resources:
❌ 如果不需要自定义域名，可以留空
```

#### 不推荐的配置
```
❌ 使用 Global API Key
❌ 给予过多权限 (如 Zone:Edit)
❌ 包含所有账户的权限
```

### Token 管理

1. **定期轮换**
   - 建议每 90 天轮换一次 API Token
   - 在 GitHub Secrets 中更新新的 Token

2. **监控使用**
   - 在 Cloudflare Dashboard 中监控 Token 使用情况
   - 发现异常活动立即撤销 Token

3. **安全存储**
   - 只在 GitHub Secrets 中存储
   - 不要在代码中硬编码
   - 不要在日志中输出

## 🔐 GitHub Secrets 安全

### 必需的 Secrets

| Secret 名称 | 描述 | 获取方式 |
|------------|------|----------|
| `CLOUDFLARE_API_TOKEN` | Cloudflare API Token | Cloudflare Dashboard → API Tokens |
| `CLOUDFLARE_ACCOUNT_ID` | Cloudflare 账户 ID | Cloudflare Dashboard → 右侧边栏 |

### Secrets 管理

1. **访问控制**
   - 只有仓库管理员可以管理 Secrets
   - 定期审查谁有访问权限

2. **环境隔离**
   - 生产环境和测试环境使用不同的 Token
   - 使用不同的 Cloudflare 项目

3. **审计日志**
   - GitHub 会记录 Secrets 的使用情况
   - 定期检查 Actions 日志

## 🚨 安全风险与缓解措施

### 潜在风险

1. **API Token 泄露**
   - **风险**: 攻击者可能修改或删除 Pages 项目
   - **缓解**: 使用最小权限 Token，定期轮换

2. **未授权部署**
   - **风险**: 恶意代码被部署到生产环境
   - **缓解**: 启用分支保护，要求代码审核

3. **依赖包风险**
   - **风险**: 恶意依赖包可能窃取 Token
   - **缓解**: 使用 `npm ci`，定期更新依赖

### 安全检查清单

部署前确认：
- [ ] API Token 使用最小权限
- [ ] 启用了分支保护规则
- [ ] 代码经过审核
- [ ] 依赖包是最新版本
- [ ] 没有硬编码的敏感信息

## 🔍 监控与审计

### 监控指标

1. **部署频率**
   - 异常的部署频率可能表示安全问题
   - 设置部署通知

2. **构建日志**
   - 检查构建日志中的异常信息
   - 关注依赖包的下载情况

3. **访问日志**
   - 监控网站的访问模式
   - 发现异常流量

### 审计步骤

1. **定期检查**
   - 每月检查 API Token 使用情况
   - 审查 GitHub Actions 日志
   - 检查 Cloudflare Pages 部署历史

2. **安全扫描**
   - 使用 GitHub 的安全扫描功能
   - 检查依赖包漏洞
   - 运行代码安全扫描

## 🚀 安全部署流程

### 标准部署流程

1. **开发阶段**
   ```bash
   # 在功能分支开发
   git checkout -b feature/new-feature
   # 提交代码
   git commit -m "feat: add new feature"
   ```

2. **代码审核**
   ```bash
   # 创建 Pull Request
   # 等待代码审核
   # 通过后合并到 main
   ```

3. **自动部署**
   ```bash
   # GitHub Actions 自动触发
   # 构建项目
   # 部署到 Cloudflare Pages
   ```

### 紧急部署流程

1. **热修复**
   ```bash
   # 创建热修复分支
   git checkout -b hotfix/critical-fix
   # 修复问题
   git commit -m "hotfix: fix critical issue"
   # 快速合并到 main
   ```

2. **回滚**
   ```bash
   # 如果需要回滚
   git revert <commit-hash>
   git push origin main
   ```

## 📞 安全事件响应

### 发现安全问题时

1. **立即行动**
   - 撤销相关的 API Token
   - 检查最近的部署记录
   - 通知团队成员

2. **调查分析**
   - 分析攻击向量
   - 检查受影响的范围
   - 收集证据

3. **修复措施**
   - 修复安全漏洞
   - 更新安全配置
   - 加强监控

### 联系方式

- **安全事件**: 立即联系开发团队
- **技术问题**: 创建 GitHub Issue
- **紧急情况**: 使用团队紧急联系方式

---

**记住**: 安全是一个持续的过程，需要定期审查和更新安全配置。
