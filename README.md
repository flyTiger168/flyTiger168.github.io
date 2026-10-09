# Tiger 的博客

博客地址：https://flytiger168.github.io/

English homepage: https://flytiger168.github.io/en/

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

## 中英文文章

导航栏的 **中文 / English** 可切换语言。中文和英文首页分别只显示对应语言的文章；同一篇文章的译文通过相同的 `translation_key` 关联。

例如，发布一篇双语文章，需要创建两个文件。两份正文分别自行填写，网站不会自动翻译文章。

中文文件：`_posts/2026-10-10-my-notes.md`

```markdown
---
layout: post
title: "我的笔记"
lang: zh-CN
translation_key: my-notes
permalink: /posts/my-notes/
date: 2026-10-10 00:00:00 +0800
excerpt: "文章的中文介绍。"
---

中文正文。
```

英文文件：`_posts/2026-10-10-my-notes-en.md`

```markdown
---
layout: post
title: "My notes"
lang: en
translation_key: my-notes
permalink: /en/posts/my-notes/
date: 2026-10-10 00:00:00 +0800
excerpt: "An introduction to this post."
---

English content.
```

`translation_key` 在同一对译文中保持一致，在不同文章之间使用不同值。两个 `permalink` 必须不同。可以先发布单一语言；暂无译文时，语言切换链接会指向另一种语言的首页。

`_data/locales.yml` 保存中英文博客名称、导航文字、日期格式和页脚介绍。修改博客名称和介绍时，同步修改这里以及 `_config.yml`。`en/about.md` 是英文关于页面，`en/index.md` 是英文首页介绍。RSS 同时包含两个语言的文章。

## Writing in English

Create a Markdown file under `_posts/` with a filename such as `2026-10-10-my-notes-en.md`. Use the English front matter example above, replace the date with the actual publication date, and write the body in English. Commit it to `main` to publish.

Use the same `translation_key` as the Chinese version to link the two translations. Each version needs a unique `permalink`. You can publish in just one language; the language switch then links to the other language's homepage. Translations are supplied by the author.

## 添加图片

将图片上传到 `assets/images/`，在文章中使用：

```markdown
![图片说明](/assets/images/example.png)
```

## 查看发布结果

在仓库的 **Actions** 页面查看 `pages build and deployment` 是否成功。
在 **Settings → Pages** 查看网站地址和发布设置。

首次发布或更新可能需要几分钟。仓库和发布后的文章均为公开内容。
