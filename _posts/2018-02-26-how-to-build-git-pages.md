---
layout: post
title: 如何搭建静态博客
subtitle: github page实战本博客
date: 2018-02-26
author: Veni
tags: jekyll 博客

---


### 方案选择
目前主流的博客搭建方案

1. 云服务器
2. 博客平台
3. Github pages

第一种相对复杂，需要自己购买云服务器（如果家里自建需要固定IP），需要一定专业基础。优点是可以建设比较复杂的动态网站，图片、文件、视频等多媒体存储方案可以自由定制无限制，并且私密性高；缺点是服务器需要定期付费，服务组件需要自己维护和运维，seo搜索需要自己做，经济和时间成本最高。

第二种最简单，方便简单，前提是选择靠谱的平台。目前技术类的CSDN，cnblogs是超过10年的博客平台，可以优先采用。特别是cnblogs可以定制主题，⚠️注意定期做好备份。

第三种Geeker优先，通过git管理发布，维护成本比较低，而且可迁移程度高。


### 实战Github pages
#### 主题模版
可参考,hugo号称目前最快静态web engine
* [hugo](https://gohugo.io/)
* [beautiful-jekyll](https://github.com/daattali/beautiful-jekyll)
* [jekyll-theme-H2O](https://github.com/kaeyleo/jekyll-theme-H2O)


#### 具体操作
[github_pages](https://docs.github.com/cn/free-pro-team@latest/github/working-with-github-pages/creating-a-github-pages-site)

### 媒体资源
#### 图床
阿里/新浪 cdn图床。优点是随时上传，方便免费，缺点是可能失效。
这里我使用七牛云的免费对象存储
#### 视频集
上传到优酷/youtube等视频平台，注意广告屏蔽

### 自定义域名管理
如果想用自己的域名绑定博客，可以借鉴下面方法。
#### 域名注册
Godaddy
国内云厂商——阿里云/腾讯云

#### 域名解析
可以选择域名服务商的解析服务
我选用腾讯云DNS(dnspod)，境内外解析IP分配(过多级子域名需要付费)
配置操作如下，记录类型CNAME

* @符号的是指定你的域名xxx.com映射到xxx.github.io，
* www那一条是指定你的主域名www.xxx.com映射到xxx.github.io。这边看别人配置的时候都说一定不要忘记xxx.github.io.后面的.


### 安全证书

免费版：Let's Encrypt
付费的挺多 Geotrust， Symantec， 阿里云/腾讯云（云厂商有时也有免费ssl）等，
