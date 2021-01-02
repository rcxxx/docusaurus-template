# Docusaurus

这个站点模板是基于 [Docusaurus 2](https://v2.docusaurus.io/) 构建的

目的是为了让需要的人快速的构建自己的静态网站

也是为了让实验室爱折腾的小伙伴一起构建起实验室的知识库

## 自定义配置

此模板的主题结构如下

``` console
my-website
├── blog
│   └── hello-world.md
├── docs
│   └── template.md
├── docusaurus.config.js
├── README.md
├── sidebars.js
└── ...
```

- `docusaurus.config.js` 为配置文件，用来配置站点
- `/blog` 中为博客文章
- `/docs` 中为文档页文章
  - `sidebar.js` 为文档页的配置文件，用来配置文档的目录

### 配置站点信息
在 `docusaurus.config.js` 文件中常用的设置项我已经添加了注释，可以根据自己的需求进行配置

### 写博文（blog）

写博客就在 `/blog` 目录下创建一个 `.md` 格式的文件，大致样式如下，前页中的内容尽量不要缺省

``` console
---
slug: hello-blog                   # 访问此篇博客时的 url
title: 第一篇博客                    # 博客标题
author: 作者                        # 作者
author_title: 作者的介绍             # 作者的标签
author_url:                        # 作者的网址
author_image_url:                  # 作者头像的链接
tags: [blog, docusaurus]           # 标签
---

标题和预览部分

<!--truncate-->

正文
```

### 写文档（docs）

写文档就在 `/docs` 目录下创建一个 `.md` 格式的文件，然后在 `sidebar.js` 文件中添加文档的 `id`

文档的前页样式如下

``` console
---
id: template                       # 文章的 id 用在 sidebar 中设置目录
title: 模板文档                     # 标题
slug: /                            # 仅落地页需要加此行
---
```

## 部署到 Vercel

在 [**Vercel**](https://vercel.com/) 注册一个账户，导入相应的 GitHub 仓库，并选择 `Docusaurus V2` 框架进行部署即可。

【待补充细节】

## 参考与致谢
- [使用 Docusaurus 搭建个人博客](https://www.zxuqian.cn/deploy-a-docusaurus-site)

- [使用 Docusaurus 搭建个人知识库](https://sinnammanyo.cn/docs/docs/about-build)

- [将 Docusaurus 部署到 GitHub Pages](https://sinnammanyo.cn/docs/docs/about-deploy)