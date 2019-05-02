---
# Copyright (c) 2019 Windy Darian
# CC-BY-NC-SA-4.0
layout: post
title: Switched to Jekyll!
image: /assets/post_images/2019-04-30-jekyll.png
image_width: 256px
---

{:.ln-en}
I switched to Jekyll and moved all data over!

{:.ln-zh}
窝开始用Jekyll了！

<!--more-->

{:.ln-en}
Now I have a GitHub repository for my blog at
[here](https://github.com/WindyDarian/workhouse)! The old posts
before this are still accessible from the
[archived list]({% link pages/all_posts.md %}).

{:.ln-zh}
把之前的数据都转移到了Jekyll，甚至放到了GitHub上
（[这里](https://github.com/WindyDarian/workhouse)）。为了方便阅读（和掩盖黑历史！）
比这篇博客更早的文章[可以在这里找到]({% link pages/all_posts.md %})。

{:.ln-en}
It had been a while since I last posted. By a while, I mean 2 years and 3
months. (I need to think about why.) I still had to do the routine maintenance
on the server regularly, because I was using WordPress. Every once in a while I
had to:

{:.ln-zh}
已经很久没有写过博客了。(很久指两年零三个月。）然而因为用的是自搭的WordPress，即使在没
写博客的这段时间，窝也必须时不时地维护VPS服务器，以下是例行维护时需要做的事情：

{:.ln-en}
> 1. Log in to my vps server with SSH.
> 2. Turn off Apache.
> 3. Update the software packages.
> 4. Turn on Apache.
> 5. Log in to WordPress backend. Check if there are new version of WordPress (and plugins and themes).
> 6. Allow Apache user to write WordPress folder.
> 7. Update WordPress.
> 8. Disallow Apache user to write WordPress folder.
>  * (In the beginning of time I didn't do this. Then my blog got destroyed by someone once, and it had to recover with a backup from a month or so before...)
> 9. ...

{:.ln-zh}
> 1. SSH登录
> 2. 关掉Apache
> 3. 更新软件
> 4. 开Apache
> 5. 登录到WordPress后台，确认WordPress、主题、插件的新版本
> 6. 赋予Apache用户WordPress文件夹的写权限
> 7. 更新WordPress
> 8. 回收Apache用户WordPress文件夹的写权限
> 9. 。。。

{:.ln-en}
I wrote scripts to automate some of the things but, anyway, I am getting tired
of doing these. I am not very a weby engineer ("but a gamey one!"), and I was
just to lazy to replace it with another thing. But I realized I need something
to save me from the labor.

{:.ln-zh}
虽然写了脚本让事情轻松很多，需要手动做的事情还是很繁琐。即使如此窝也就这样用了很久的
WordPress毕竟窝不是经常做web相关的码农（还是做游戏最棒！）。终于厌烦了重复劳动，决定
找新的解决方案。

{:.ln-en}
I like version control tools, especially git since it's decentralized and easy
to backup (by just `git clone`). I cannot live without them. However with
WordPress and the blog data in mysql database, it didn't feel I was controlling
them... Plus I want to use my favorite text editor, and markdown.

{:.ln-zh}
窝喜欢版本控制软件，尤其是git。它在版本管理的同时还是去中心化的，也就是说每一个克隆了
仓库的电脑都是一个有完整历史的备份。总之用git是非常开心的一件事！然而在WordPress里就
找不到这样的快乐了:(... 此外，如果能用窝喜欢的文本编辑器那最好不过。

{:.ln-en}
So I made the switch!

{:.ln-zh}
窝不用WordPress啦！

[![俺はWordpressをやめるぞ！]({{page.image}}){:width="256px"}]({{page.image}})

{% comment %}
	TODO?: thumbnails? Auto link image to itself?
{% endcomment %}
