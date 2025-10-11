# 🚀 完全自动化部署配置

本配置实现了完全自动化的部署流程，任何人对仓库的更改都会自动触发部署。

## ⚡ 自动化流程

### 主分支 (main) 推送
```
开发者推送代码 → GitHub Actions 构建 → 自动部署到生产环境 → 网站实时更新
```

### Pull Request
```
创建 PR → GitHub Actions 构建检查 → 生成预览链接 → 审核通过后合并 → 自动部署
```

## 🔧 配置步骤

### 1. GitHub 仓库设置

#### 添加 Secrets
在 GitHub 仓库设置中添加以下 Secrets：

1. **CLOUDFLARE_API_TOKEN**
   - 获取方式：Cloudflare Dashboard → My Profile → API Tokens → Create Token
   - 权限：Zone:Zone:Read, Zone:Zone Settings:Read, Account:Cloudflare Pages:Edit
   - 作用域：Include:All zones

2. **CLOUDFLARE_ACCOUNT_ID**
   - 获取方式：Cloudflare Dashboard → 右侧边栏 "Account ID"
   - 用于标识您的 Cloudflare 账户

#### 设置步骤：
1. 进入 GitHub 仓库
2. 点击 Settings → Secrets and variables → Actions
3. 点击 "New repository secret"
4. 添加上述两个 secrets

### 2. Cloudflare Pages 设置

#### 通过 Dashboard 配置：
1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 进入 Pages → 创建项目
3. 连接 GitHub 仓库
4. 配置构建设置：
   ```
   项目名称: sensecraft-hmi-docs
   生产分支: main
   框架预设: Astro
   构建命令: npm run build
   构建输出目录: dist
   Node.js 版本: 18
   ```

#### 启用自动部署：
- ✅ 自动部署：启用
- ✅ 预览部署：启用
- ✅ 分支部署：启用

### 3. 分支策略（推荐）

```
main (生产环境)
├── 自动部署到生产环境
├── 需要 Pull Request 合并
└── 受保护分支

develop (开发环境)
├── 自动生成预览部署
├── 用于功能开发
└── 定期合并到 main

feature/* (功能分支)
├── 自动生成预览部署
├── 用于新功能开发
└── 完成后合并到 develop
```

## 🔄 自动化工作流

### 工作流 1: 生产部署 (deploy.yml)
**触发条件：**
- 推送到 `main` 分支
- 创建 Pull Request

**执行步骤：**
1. 检出代码
2. 设置 Node.js 18
3. 安装依赖
4. 构建项目
5. 部署到 Cloudflare Pages

### 工作流 2: 构建检查 (build-check.yml)
**触发条件：**
- 推送到任何分支
- 创建 Pull Request

**执行步骤：**
1. 构建项目
2. 验证构建输出
3. 上传构建产物
4. 提供构建状态反馈

## 📊 部署状态监控

### GitHub Actions 状态
- 在仓库首页可以看到构建状态
- 绿色 ✅ = 构建成功
- 红色 ❌ = 构建失败

### Cloudflare Pages 状态
- 在 Cloudflare Dashboard 查看部署历史
- 每个部署都有唯一 URL
- 可以查看构建日志

### 通知设置
1. **GitHub 通知**
   - 设置 → Notifications → Actions
   - 选择接收构建状态通知

2. **Cloudflare 通知**
   - 在 Pages 项目设置中配置
   - 可以设置邮件通知

## 🚨 故障排除

### 常见问题

#### 1. 构建失败
**症状：** GitHub Actions 显示红色状态
**解决：**
```bash
# 本地测试构建
npm run build

# 检查错误日志
# 修复代码问题后重新推送
```

#### 2. 部署失败
**症状：** Cloudflare Pages 部署失败
**解决：**
- 检查 `CLOUDFLARE_API_TOKEN` 权限
- 验证 `CLOUDFLARE_ACCOUNT_ID` 正确性
- 查看 Cloudflare 构建日志

#### 3. 权限问题
**症状：** GitHub Actions 无法访问 Cloudflare
**解决：**
- 重新生成 API Token
- 检查 Token 权限范围
- 确认 Account ID 正确

### 调试命令
```bash
# 本地测试完整流程
npm ci
npm run build
npm run preview

# 检查构建输出
ls -la dist/

# 验证配置文件
cat .github/workflows/deploy.yml
cat wrangler.toml
```

## 📈 性能优化

### 构建优化
- 使用 npm ci 而不是 npm install
- 启用 Node.js 缓存
- 并行执行构建步骤

### 部署优化
- 只部署必要的文件
- 使用 CDN 缓存
- 启用压缩

## 🔐 安全考虑

### API Token 安全
- 使用最小权限原则
- 定期轮换 Token
- 不要在代码中硬编码

### 分支保护
- 启用分支保护规则
- 要求 Pull Request 审核
- 要求状态检查通过

## 📋 检查清单

部署前确认：
- [ ] GitHub Secrets 已配置
- [ ] Cloudflare Pages 项目已创建
- [ ] 自动部署已启用
- [ ] 构建命令正确
- [ ] 输出目录正确
- [ ] Node.js 版本匹配

## 🎯 最佳实践

1. **提交信息规范**
   ```
   feat: 添加新功能
   fix: 修复问题
   docs: 更新文档
   style: 代码格式调整
   refactor: 代码重构
   ```

2. **分支命名规范**
   ```
   feature/功能名称
   bugfix/问题描述
   hotfix/紧急修复
   ```

3. **Pull Request 规范**
   - 清晰的标题和描述
   - 关联相关 Issue
   - 添加测试说明
   - 请求代码审核

## 📞 支持

如果遇到问题：
1. 查看 GitHub Actions 日志
2. 检查 Cloudflare Pages 构建日志
3. 参考本文档的故障排除部分
4. 联系开发团队

---

**配置完成后，您的文档站点将实现完全自动化部署！** 🎉
