# Hexo基本操作

Hexo是一个快速、简洁且高效的静态博客框架，使用Markdown语法编写文章，可以方便地生成静态网页。

## 写作

你可以执行下列命令来创建一篇新文章或者新的页面。

$ hexo new [layout] <title>
您可以在命令中指定文章的布局（layout），默认为 post，可以通过修改 _config.yml 中的 default_layout 参数来指定默认布局。

布局（Layout）
Hexo 有三种默认布局：post、page 和 draft。在创建这三种不同类型的文件时，它们将会被保存到不同的路径；而您自定义的其他布局和 post 相同，都将储存到 source/_posts 文件夹。

布局    路径
post    source/_posts
page    source
draft    source/_drafts

## 快速开始

#### 前置条件

`node版本 14.21.3 yarn版本 1.22.21`
安装依赖
`yarn`
安装hexo
`yarn global add hexo-cli`
如果是mac系统 需要修改环境变量
在`~/.zshrc` 中加入如下配置
在终端中输入`open ~/.zshrc`输入一下命令并保存
`export PATH=$PATH:$(yarn global bin)`
保存文件后，在终端中运行以下命令使其生效
`source ~/.zshrc`
hexo server  或 yarn server 即可开始

开始写作 
`hexo new [layout] <title>` 默认创建`<title>.md`文件 无需额外写.md格式
例如`hexo new 模版` 创建出模版.md

在md文件顶部写入yml格式配置 可以对文档进行配置

详细配置可以查看 _config.icarus.yml 
文档基础设置例子

```yml
--- 
title: vercel + hexo 搭建个人博客并绑定域名 # 标题
toc: true # 侧边栏展示文章目录
cover: ../img/blog1_vercel_hexo/blog1_vercel_hexo_9.png # 封面
tags: # 标签
    - 域名
    - markdown
categories: # 分类
    - 教程
date: 2023-03-29 20:16:39
---
```