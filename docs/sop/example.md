---
description: md头部标签说明
title: 文章内容头部标签说明
readingTime: false
recommend: 5
hidden: true
sticky: 998
---

# 文章头部说明

- title: 标题
> 不设置情况下默认取一级标题 # 一级标题

- description: 描述信息
> 用于设置文章在首页卡片列表里展示，不设置的情况下，默认取文章内容的前100个字符

- descriptionHTML: 描述信息
> 使用自定义的HTML内容设置文章在首页卡片列表里展示

- cover: 封面信息
> 用于设置文章在首页卡片列表里展示的，未指定时，默认取文章中出现的第一张图片，同时如果手动设置了，封面将同时在文章页展示
> 可以通过下面的 hiddenCover 隐藏文章页的展示

- hiddenCover: 文章的封面
> 控制是否展示当前文章的封面，全局配置开关见 article.hiddenCover
- hidden: 文章的封面
> 用于设置文章是否出现在首页的列表里

- author: 作者信息
> 用于单独设置文章的作者信息
> 如果没有单独设置则会默认使用全局的 author 配置
- readingTime: 阅读时间
> 单独设置是否展示文章的预计阅读时间, 全局配置开关见 article.readingTime
- comment: 评论
> 单独为某篇文章设置是否开启评论
- date: 发布时间
> 单独设置文章的发布时间，不设置的情况下默认会通过Git取文件最后修改时间，设置为 false 则不会在文章页展示

- tag / tags / categories: 标签
> 用于按标签给文章分类，同时，在文章页标签可点击跳转
```md
---
tag:
 - 日志
tags:
 - 信息
categories:
 - 测试分类
---
```

- sticky: 精选文章
> 用于设置在首页展示，值越大展示越靠前

- top: 首页置顶
> 用于设置在首页置顶展示的文章，从 1 开始，值越小越靠前

- recommend: 左侧推荐列表
> 可用于配置左侧推荐列表数据表现，默认只展示同级目录下的文章
> - 文章左侧展示的 推荐文章 顺序（越小越靠前）
> - 在推荐列表中隐藏掉不展示
> - 手动关联不同目录的文章进行展现
:::=tabs
::只调整顺序
```md
---
recommend: 1
---
```

::在列表中隐藏
```md
---
recommend: false
---
```

::自定义关联
```md
---
# 直接设置文章的关键词
recommend: 'Node.js'
# 设置多个关键词
recommend: ['Node.js', 'css', 'html']
# 设置关键词并设置顺序
recommend: ['Node.js', 'css', 'html', 1]
---
```
:::


- publish: 发布
> 表明文章是否发布，用于设置文章是否出现在首页和侧边栏里
```md
---
publish: false
---
```
等价于
```md
---
hidden: true
recommend: false
---
```

- buttonAfterArticle: 文章底部按钮
> 用于单独控制某篇文章底部按钮，点击按钮会在按钮下方渲染一个自定义的html内容，例如可以用来做赞赏按钮，内置了 wechatPay 和 aliPay 两个图标，也可自定义图标(svg)。
```md
---
buttonAfterArticle:
  openTitle: 投币
  closeTitle: 下次一定
  content: '<img src="https://img.cdn.sugarat.top/mdImg/MTY0Nzc1NTYyOTE5Mw==647755629193">'
  icon: aliPay
  # size: small
  # expand: true
---
```

 