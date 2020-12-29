# Docusaurus

这个站点模板是基于[Docusaurus 2](https://v2.docusaurus.io/)构建的

目的是为了让需要的人快速的构建自己的静态网站

也是为了让实验室爱折腾的小伙伴一起构建起实验室的知识库

## 配置环境

#### nodejs >= 10.15.1
- [nodejs下载](https://nodejs.org/en/download/)

#### yarn >= 1.5
- [yarn下载](https://classic.yarnpkg.com/en/)

## 安装

``` bash
yarn install
```

## 本地预览

``` bash
yarn start
```

将自动在你的浏览器中启动站点的预览，并可以实时编辑，应用更改

## 自定义配置

此模板的主题结构如下

``` console
my-website
├── .github
│   └── workflows
│       └── doc-action.yml
├── blog
│   └── hello-world.md
├── docs
│   └── template.md
├── package.json
├── src
│   ├── css
│   │   └── custom.css
│   └── pages
│       ├── styles.module.css
│       └── index.js.bak
├── static
│   └── img
├── docusaurus.config.js
├── package.json
├── README.md
├── sidebars.js
└── yarn.lock
```

- `docusaurus.config.js` 为配置文件，用来配置站点
- `/blog` 中为博客文章
- `/docs` 中为文档页文章
  - `sidebar.js` 为文档页的配置文件，用来配置文档的目录

### 配置站点信息
在 `docusaurus.config.js` 文件中常用的设置项我已经添加了注释，可以根据自己的需求进行配置

### 编辑
写博客就在 `/blog` 中创建一个 `markdown` 文件，大致样式如下，前页中的内容尽量不要缺省

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

写文档就在 `/docs` 中创建一个 `markdown` 文件，然后在 `sidebar.js` 文件中添加文档的 `id`

文档的前页样式如下

``` console
---
id: template                       # 文章的 id 用在 sidebar 中设置目录
title: 模板文档                     # 标题
sidebar_label: template            # 侧边栏标题
slug: /                            # 访问文章时的 url 不设置则默认为 id
---
```

## 构建

``` bash
yarn build
```

这个命令生成静态内容到“构建”目录，可以使用任何静态内容托管服务

## 部署到GitHub Pages
对 `docusaurus.config.js` 中的相关内容进行配置

``` js
url: 'https://github.com/username/projectName/',
baseUrl: '/projectName/',
organizationName: 'username', // Usually your GitHub org/user name.
projectName: 'projectName', // Usually your repo name.
```

名称               | 描述
-------------------|-------------------------
`organizationName` | GitHub用户名
`projectName`      | GitHub存储库的名称
`url`              | GitHub页面的URL
`baseUrl`          | 项目的基本URL，填 /projectName/

都配置好之后，就可以将 **`Docusaurus`** 部署到 **`GitHub Pages`** 上了，执行
``` bash
GIT_USER=<GITHUB_USERNAME> yarn deploy
```
等待运行完成就部署完成了，就可以通过你配置好的 **`url`** 访问你的页面了



## 参考与致谢
- [使用 Docusaurus 搭建个人博客](https://www.zxuqian.cn/deploy-a-docusaurus-site)

- [使用 Docusaurus 搭建个人知识库](https://sinnammanyo.cn/docs/docs/about-build)

- [将 Docusaurus 部署到 GitHub Pages](https://sinnammanyo.cn/docs/docs/about-deploy)