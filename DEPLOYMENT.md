# Cloudflare Pages 部署指南

本指南将帮助您将 SenseCraft HMI 文档站点部署到 Cloudflare Pages。

## 🚀 部署方式

### 方式一：通过 Cloudflare Dashboard（推荐）

1. **登录 Cloudflare Dashboard**
   - 访问 [Cloudflare Dashboard](https://dash.cloudflare.com/)
   - 登录您的账户

2. **创建新的 Pages 项目**
   - 点击左侧菜单中的 "Pages"
   - 点击 "创建项目" 或 "Create a project"
   - 选择 "连接到 Git" 或 "Connect to Git"

3. **连接 GitHub 仓库**
   - 选择 GitHub 作为 Git 提供商
   - 授权 Cloudflare 访问您的 GitHub 账户
   - 选择 `Seeed-Solution/sensecraft-hmi-docs` 仓库

4. **配置构建设置**
   ```
   项目名称: sensecraft-hmi-docs
   生产分支: main
   框架预设: Astro
   构建命令: npm run build
   构建输出目录: dist
   ```

5. **环境变量（可选）**
   - 如果需要在构建时使用环境变量，可以在 "环境变量" 部分添加
   - 例如：`NODE_VERSION=18`

6. **部署**
   - 点击 "保存并部署" 或 "Save and Deploy"
   - Cloudflare 将自动构建并部署您的站点

### 方式二：通过 Wrangler CLI

1. **安装 Wrangler**
   ```bash
   npm install -g wrangler
   ```

2. **登录 Cloudflare**
   ```bash
   wrangler login
   ```

3. **部署到 Pages**
   ```bash
   # 构建项目
   npm run build
   
   # 部署到 Pages
   wrangler pages deploy dist --project-name sensecraft-hmi-docs
   ```

## ⚙️ 配置说明

### 构建配置
- **Node.js 版本**: 18.x 或更高
- **构建命令**: `npm run build`
- **输出目录**: `dist`
- **框架**: Astro (静态站点生成)

### 文件说明
- `_headers`: 配置 HTTP 响应头，包括缓存和安全策略
- `_redirects`: 配置 URL 重定向规则
- `wrangler.toml`: Cloudflare Wrangler 配置文件

### 自定义域名
1. 在 Cloudflare Pages 项目设置中
2. 点击 "自定义域名" 或 "Custom domains"
3. 添加您的域名（如 `docs.sensecraft-hmi.com`）
4. 按照指示配置 DNS 记录

## 🔧 环境变量

如果需要设置环境变量，可以在 Cloudflare Pages 项目设置中添加：

| 变量名 | 值 | 说明 |
|--------|-----|------|
| `NODE_VERSION` | `18` | Node.js 版本 |
| `PUBLIC_SITE_URL` | `https://docs.sensecraft-hmi.com` | 站点 URL |

## 📊 性能优化

### 缓存策略
- 静态资源（CSS、JS、图片）：缓存 1 年
- HTML 页面：缓存 1 小时
- 图片文件：缓存 1 个月

### 安全头
- `X-Frame-Options: DENY`
- `X-Content-Type-Options: nosniff`
- `Referrer-Policy: strict-origin-when-cross-origin`

## 🚨 故障排除

### 常见问题

1. **构建失败**
   - 检查 Node.js 版本是否为 18+
   - 确保所有依赖都已正确安装
   - 查看构建日志中的错误信息

2. **页面无法访问**
   - 检查自定义域名配置
   - 确认 DNS 记录设置正确
   - 验证 SSL 证书状态

3. **资源加载失败**
   - 检查 `_headers` 文件配置
   - 确认资源路径正确
   - 验证缓存设置

### 调试命令
```bash
# 本地构建测试
npm run build
npm run preview

# 检查构建输出
ls -la dist/

# 验证配置文件
cat _headers
cat _redirects
```

## 📈 监控和分析

### Cloudflare Analytics
- 在 Cloudflare Dashboard 中查看访问统计
- 监控页面加载性能
- 分析用户行为数据

### 自定义分析
可以在 `astro.config.mjs` 中添加 Google Analytics 或其他分析工具：

```javascript
head: [
  // ... 其他配置
  {
    tag: 'script',
    attrs: {
      src: 'https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID',
      async: true,
    },
  },
  {
    tag: 'script',
    content: `
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      gtag('config', 'GA_MEASUREMENT_ID');
    `,
  },
]
```

## 🔄 自动部署

### GitHub Actions（可选）
可以设置 GitHub Actions 来自动部署：

```yaml
# .github/workflows/deploy.yml
name: Deploy to Cloudflare Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: npm ci
      - run: npm run build
      - uses: cloudflare/pages-action@v1
        with:
          apiToken: ${{ secrets.CLOUDFLARE_API_TOKEN }}
          accountId: ${{ secrets.CLOUDFLARE_ACCOUNT_ID }}
          projectName: sensecraft-hmi-docs
          directory: dist
```

## 📞 支持

如果遇到部署问题，可以：
1. 查看 Cloudflare Pages 构建日志
2. 检查 GitHub Issues
3. 联系开发团队

---

**最后更新**: 2024年1月  
**维护者**: Seeed Studio 文档团队
