# utowo's blog

个人博客，使用 [Astro](https://astro.build/) + [Fuwari](https://github.com/saicaca/fuwari) 构建，部署在 GitHub Pages。

线上地址：<https://utowo.github.io/>

## 本地开发

```bash
pnpm install
pnpm dev        # http://localhost:4321
```

## 写文章

```bash
pnpm new-post <filename>
```

文章放在 `src/content/posts/`，front matter 格式：

```yaml
---
title: 文章标题
published: 2026-11-03
description: 一句话摘要
tags: [标签]
category: 分类
draft: false
lang: zh_CN
---
```

## 构建

```bash
pnpm build      # 输出到 dist/，并生成 Pagefind 搜索索引
pnpm preview    # 本地预览构建结果
```

## 部署

推送到 `main` 分支后，GitHub Actions 会自动构建并发布到 GitHub Pages。

首次使用时需要在仓库的 **Settings → Pages → Source** 中选择 **GitHub Actions**。

旧 Hexo 站点的文章链接已通过 `public/2025/` 下的静态跳转页指向新地址。

## 配置

- 站点信息、导航、侧栏资料：`src/config.ts`
- 站点 URL：`astro.config.mjs` 中的 `site`
- 关于页：`src/content/spec/about.md`
- 图标：`public/favicon.svg`

## 许可

博客内容归作者所有；主题部分基于 [Fuwari](https://github.com/saicaca/fuwari)，MIT License。
