---
layout: post
title: 如何搭建一个令人愉快的博客
date: 2016-05-31
tags: 能工巧匠集
---
> 程序员，你有自己的博客吗？

##前言
第一篇半技术向的博客。在这篇博客里我会讲怎样利用`GitHub Page`和`Jekyll`搭建一个**令人愉快**的个人博客。

个人认为一个“令人愉快”的博客至少要有以下三个特点：
> 1.原创，或者动脑子地转载。很抱歉，这一点我做不了教程

> 2.内容丰富，坚持更新。很抱歉，这一点我也做不了教程

> 3.免费，没有广告。有靠谱的版本管理。`markdown`什么的最好了。幸运的是这一点我是可以做教程的😂

##言归正传
###GitHub Page Blog
GitHub不知道什么时候推出的（应该也挺早了？）一个服务。你可以建一个专门的Github账号，也可以用现有的账号。账号下建立一个名叫ID.github.io的repo。这样我们就可以开始愉快的玩耍啦！
>博客的域名为ID.github.io

>博文存放在repo: ID.github.io

> Github 支持的 markdown engine :kramdown(default), redcarpet

Github官方给了一些简单的博客模板，在repo的`settings`里可以找到，样式都还可以。如果对排版要求不是特别高的话，用官方的模板应该就够了

### Jekyll环境
Jekyll不配也是可以的，不过最好是在本地配一下。一是可以生成模板化的目录树，二是可以直接在本地预览。

如果本机已经有现成的ruby环境:

```
shell> gem install jekyll
```
不过大多数大陆用户默认源是用不了的。所以先要把默认源换掉:

```
shell> gem sources --remove https://rubygems.org/
shell> gem sources -a https://ruby.taobao.org/
shell> gem sources -l
```
安装完jekyll之后就可以开始写博客了。

```
shell> mkdir -p ~/my_very_handsome_blog
shell> cd my_very_handsome_blog
shell> jekyll server .
```
最后一句启动jekyll的管理进程，有点像apache。如果是一个空目录，jekyll会建立一些辅助的目录。有可能会报错，类似于提示你没装`jekyll-paginate`啊，或者`redcarpet`之类杂七杂八的依赖，直接`gem install xxxxx`就是了。访问`http://localhost:4000/`可以在本地预览博客的效果
![](/assets/images/2016/jekyll-preview.png)

###一些简单的配置
由于jekyll自动生成博客框架中有较多的默认值，并且针对github有特殊处理，所以我们在把自己的第一版博客发布到github之前需要做一些个性化配置（博客名，个人信息等）。当然，如果你觉得留着这些默认值也可直接跳过这一段，直接进行发布:) 个性化配置主要在_config.yml中进行。博文放在`_posts`文件夹下，存成`yyyy-mm-dd-blogname.md`的形式即可～
> TALK is cheap, show me the CODE!

Jekyll有蛮多有意思的模板哦，可以尝试尝试，也可以自己动手改一改，很有乐趣的。
代码我就不贴了，戳[这里](https://github.com/tianling-blog/tianling-blog.github.io)可以看我的网站源码。

把文件夹push 到Github就可以了，如果没有什么错误的话Github就会给你发一封邮件![](/assets/images/2016/github-mail.png)，访问`http://ID.github.io/`就可以看到你的blog啦

## 后记
啊终于写完了呢，Github每日commit完成✅

期末更的比较少一点，毕竟有点忙嘛。这片blog大部分是今天下午的选修课码起来的。每年期末的感觉如下：
![](/assets/images/2016/tom-is-busy.png)

就写到这儿啦～

啊对了Jekyll的文档戳[这里](http://jekyll.bootcss.com/docs/home/)

祝诸君好梦，期末加油！



