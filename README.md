# 我的博客

基于 Hexo 8 + AnZhiYu 主题，部署在 GitHub Pages 上。Butterfly 主题配置保留在 `_config.butterfly.yml`，需要回退时可在 `_config.yml` 改回 `theme: butterfly`。

## 本地开发

```bash
npm install        # 首次
npx hexo server    # http://localhost:4000
npx hexo new "标题" # 新建文章
npx hexo clean      # 清理缓存和 public/
npx hexo generate   # 生成静态文件到 public/
```

## 仓库与站点

- GitHub 仓库：<https://github.com/Robin0-cpu/r0b1n.github.io>
- 博客网址：<https://robin0-cpu.github.io/r0b1n.github.io/>
- Hexo 主题：AnZhiYu；切换主题时 Butterfly 配置保留作回退。

## 发布更新

```bash
git add .
git commit -m "更新博客"
git push
```

GitHub Actions 会自动构建并部署。

## 目录说明

| 路径 | 作用 |
|---|---|
| `source/_posts/` | 文章（Markdown） |
| `source/about/` | 关于页 |
| `_config.yml` | 站点配置 |
| `_config.anzhiyu.yml` | AnZhiYu 主题设置 |
| `_config.butterfly.yml` | Butterfly 回退配置 |
| `source/css/custom.css` | 自定义配色和样式 |
| `.github/workflows/pages.yml` | 自动部署 |
