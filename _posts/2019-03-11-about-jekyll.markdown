---
layout:     post
title:      "jekyll的使用"
subtitle:   " \"对jekyll学习的总结\""
date:       2019-03-11 16:00:00 UTC+8
author:     "王先虎"
header-img: "img/about-markdown/bg.jpg"
published: false
tags:
    - jekyll
    - 学习
    - 笔记
---

<p align='center'><font size='5'>jekyll语法总结</font></p>

## 书写格式

每写一篇blog，都要在markdown的文章开头写一些信息，有指定模板（layout）,标题（title），描述（description）,是否发布（published），以及自定义变量

```
---
layout: post
title: title
published: true 
---
```

例如想在文章中加入天气

```
---
layout: post
title: title
published: true 
weather: sunny
---
```

然后调用时只需要{{post.weather}}即可

## _config.yml文件数据的调用

_config.yml文件内的数据调用很简单只需要用site.你所需要的数据即可

## 自定义数据文件及文件内数据的调用

jekyll支持_date目录下的yaml,json,和csv格式的文件数据

例如_date下创建user.yml文件

调用时zh'xu