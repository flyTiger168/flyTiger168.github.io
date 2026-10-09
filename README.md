# Tiger 的博客

博客地址：https://flytiger168.github.io/

使用 GitHub Pages 和 Jekyll Minima 主题。发布源为 `main` 分支的仓库根目录。

## 发布文章

1. 在 GitHub 打开本仓库，点击 **Add file → Create new file**。
2. 文件名填写 `_posts/YYYY-MM-DD-英文文章名.md`，例如 `_posts/2026-10-10-my-notes.md`。
3. 使用下面的格式填写内容，将日期替换为实际发布日期。
4. 点击 **Commit changes**，提交到 `main` 分支，等待 GitHub Pages 自动发布。

```markdown
---
layout: post
title: "文章标题"
date: 2026-10-10 00:00:00 +0800
excerpt: "一句话介绍这篇文章。"
---

这里写正文。

## 小标题

继续写内容。
```

未来日期的文章默认不会发布。文章网址格式为 `/posts/英文文章名/`。

## 修改博客

- `_config.yml`：博客名称、介绍、作者与主题设置。
- `index.md`：首页介绍，文章列表由主题自动生成。
- `about.md`：关于页面。
- `_posts/`：博客文章。
- `assets/main.scss`：中文字体与样式。

## 添加图片

将图片上传到 `assets/images/`，在文章中使用：

```markdown
![图片说明](/assets/images/example.png)
```

## 查看发布结果

在仓库的 **Actions** 页面查看 `pages build and deployment` 是否成功。
在 **Settings → Pages** 查看网站地址和发布设置。

首次发布或更新可能需要几分钟。仓库和发布后的文章均为公开内容。
