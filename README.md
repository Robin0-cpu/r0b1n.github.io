# 我的博客

基于 Hexo 8 + Butterfly 主题，部署在 GitHub Pages 上。

## 本地开发

```bash
npm install        # 首次
npx hexo server    # http://localhost:4000
npx hexo new "标题" # 新建文章
npx hexo clean      # 清理缓存和 public/
npx hexo generate   # 生成静态文件到 public/
```

## 上线前必须改的两处

1. `_config.yml` 里的 `url`：把 `YOUR_USERNAME` 换成你的 GitHub 用户名。
   - 仓库名是 `<用户名>.github.io` → `https://<用户名>.github.io`，`root: /`
   - 仓库名是别的（如 `blog`）→ `https://<用户名>.github.io/blog`，`root: /blog/`
2. `source/about/index.md` 里的 GitHub 链接和邮箱，以及 `_config.butterfly.yml` 里 `social` 的 GitHub 地址。

## 发布

先在仓库 **Settings → Pages → Source** 选择 **GitHub Actions**，再推代码：

```bash
git init
git add .
git commit -m "init blog"
git branch -M main
git remote add origin https://github.com/<用户名>/<仓库名>.git
git push -u origin main
```

等 Actions 跑完即可访问 `https://<用户名>.github.io`。如果先 push 后开 Pages，去 Actions 页面点一次 **Re-run** 即可。

## 目录说明

| 路径 | 作用 |
|---|---|
| `source/_posts/` | 文章（Markdown） |
| `source/about/` | 关于页 |
| `_config.yml` | 站点配置 |
| `_config.butterfly.yml` | 主题配置 |
| `.github/workflows/pages.yml` | 自动部署 |
