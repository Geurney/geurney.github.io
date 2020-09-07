---
layout: post
title: "如何用GitHub Pages搭建个人Blog"
date: 2020-09-06 21:30:00
description: "Windows下使用GitHub Pages搭建个人Blog并使用jekyll-clean-dark主题"
toc: true
tags:
- github
---



## 创建仓库
[官方教程](https://docs.github.com/cn/github/working-with-github-pages/creating-a-github-pages-site)

首先创建一个仓库，仓库名必须为*\<user\>.github.io*。这个库就用来存储blog。

在仓库的Settings->GitHub Pages里会显示站点的URL为*https://\<user\>.github.io*, 这样就搭建好了。

在**根目录**下，创建index.html/index.md。或者直接使用下面的主题。

注意：

GitHub Pages默认使用静态站点生成器Jekyll，不支持服务器端语言，例如PHP、Ruby或Python。

- GitHub Pages 源仓库建议的限制为1GB
- 发布的 GitHub Pages 站点不得超过1GB
- GitHub Pages 站点的软带宽限制为每月100G。
- GitHub Pages 站点的软限制为每小时10次构建

最后安装[GitHub Desktop](https://desktop.github.com/), 将仓库clone到本地。  



## 使用jekyll-clean-dark主题
[GitHub链接](https://github.com/streetturtle/jekyll-clean-dark)

[演示和使用说明](http://pavelmakhov.com/jekyll-clean-dark/)

下载jekyll-clean-dark，解压到Blog所在的库。

注意：
- _posts文件夹用来存文章，文件名不能含有空格
- _config.yml是Jekyll的配置文件，baseurl要改成空
- about链接到主页的/about
- admin链接到https://\<user\>.github.io/admin/
- tags在blog的文档头可以定义，在文章中使用了新的tag后需要在tag文件夹下创建一个同名的md文件，内容为：
````
  ---
  layout: tag_index
  tag: tag_name
  ---
````  


## 使用Atom Markdown编辑器
[下载链接](https://atom.io/)

打开Atom，添加_posts和tag文件夹为project，就可以编写文章了

快捷键ctrl+shift+m打开preview窗口，可以预览文件

File->Settings->Packages 搜索Markdown Preview，在其Settings里取消Use GitHub.com style，就可以使preview也变成黑色主题  



## 编写Blog文章
参见[Markdown语法](/_posts/2020/09/06/Markdown语法)

通过Atom在_posts文件夹下新建md文件，便可以开始编写文章。写好后通过ctrl+s保存文章。    



## 发布文章
- 点击Atom右下角的Git按钮弹出git面板
- 点击右上角的Stage All，填写Commit message
- 然后点击Commit to master
- 点击右下角的push即可发布

保存文章后也可以通过GitHub Desktop发布。

刷新Blog站点网页，等待更新即可。
