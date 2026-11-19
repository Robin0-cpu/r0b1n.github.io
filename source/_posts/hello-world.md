---
title: 你好，世界
date: 2026-11-09 16:45:00
tags: [Hexo, 建站]
categories: [技术]
description: 博客的第一篇文章，顺便记一下 Hexo 的日常写法：新建文章、本地预览、代码块和图片。
---

这是博客的第一篇文章。它在 `source/_posts/hello-world.md` 里，用 Markdown 写成。

<!-- more -->

## 怎么写新文章

在项目目录执行：

```bash
npx hexo new "文章标题"
```

Hexo 会生成 `source/_posts/文章标题.md`，填好 front-matter 的 `tags`、`categories`，正文直接写 Markdown 即可。

## 本地预览

```bash
npx hexo server
```

打开 <http://localhost:4000>，保存文件后页面会自动刷新。

## 代码块长这样

```js
const hello = (name) => `你好，${name}`;
console.log(hello('世界'));
```

## 图片

把图片放到 `source/images/` 下，然后：

```markdown
![说明文字](/images/example.png)
```

就这些。删掉这篇文章，或者把它改成你自己的开场白。
