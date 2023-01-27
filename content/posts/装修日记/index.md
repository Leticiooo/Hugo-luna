---
title: "装修日记"
date: 2023-01-01T14:18:05+08:00
slug: decoration
draft: false # 是否为草稿
Toc: true # 显示目录
Summary: 坎坷艰辛的搭建旅程，被自己笨死一万次。
# type: "post" or "status"
# author: Author
# featured_image: cover.jpg
tags: 
    - Tech
categories:
  - 跌跌撞撞ing
---
## 写在前面
每次看到别人有自己的漂亮博客就好羡慕好羡慕，但秉持着“只要手头上还有比这更容易做的事就不轻易动手”的原则，一直拖拖拖拖了一整个2022……于是在2023年1月1号这一天，博主抛下了难产的年终总结以及难产的毕设中期报告，撸起袖子开始捣鼓了！  
设备与测试环境：{{< tag-outlined blue "MacBook Air 2020(M1)" >}} {{< tag-outlined blue "macOS Ventura 13.1" >}}  {{< tag-outlined blue "Chrome" >}} 
{{< hr "在这里放一个ToDo List" >}}
{{< notice success >}}
  **普通博客文章插入图片默认铺满宽度，无法调整大小（但在gallery模式就可以）**  
  丨2023-01-09更新：解决啦！实在憋不住去GitHub上给作者留了个issue，没想到很快就得到了回复！
{{< /notice >}}
  具体方法是在`/assets/sass/typo.scss`中找到第281行：  
  ```scss
    img:not(.link-card-img), 
  ```
  删去改为
  ```scss
    img {
        @apply my-4 rounded dark:border-darkBorder w-auto mx-auto max-w-[60%] #这里具体大小可以自己调整
    }
  ```
{{< notice info >}}
  **评论系统**  
  丨但因为博客没人看，可以稍后再议
{{< /notice >}}

## 前置准备
### 1. 安装Git

### 2. 安装Hugo
### 3. 配置SSH
{{< notice warn >}}
其实博主本人并不明确地知道这个步骤是否有用，因为在搭建过程中出了太多奇怪的问题，推倒重建过好几次，但这一步并没有重建。
{{< /notice >}}
验证SSH连接是否成功，继续在终端内输入
`ssh -T git@github.com`  
如果返回
```
Hi Username! You've successfully authenticated, but GitHub does not provide shell access.
```
则为连接成功。如果出现
```
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```
则输入`yes`后回车即可。  
很不幸，博主在输入yes后返回的是`git@github.com: Permission denied (publickey).`，搜索发现应该是ssh密钥出了问题，于是返回重新生成.pub文件，不知道为什么反复重试了好几次之后突然成功了（可能靠一些执着感动了它）。
## 安装主题
### 1. 挑选主题
### 2. 安装luna
### 3. 配置主题
[官方文档](https://github.com/adityatelange/hugo-PaperMod/wiki/Features)
## 托管部署(GitHub Page/Vercel)
{{< notice warn >}}
以下两种方法都可以部署，博主两种都试过之后才发现自己是非常画蛇添足地先部署到GitHub Page，再把GitHub Page部署到Vercel上（啊啊啊被自己笨死）。但其实不用这么麻烦的，两种选一种就可以了！（反正在国内这俩都不能流畅访问是吧）
{{< /notice >}}

{{< tab-view >}}
{{< tab-panel name="部署在GitHub Page上" checked=true >}}

{{< /tab-panel >}}

{{< tab-panel name="部署在Vercel上" >}}
这一步出了点问题，不知道为什么最后生成的网页界面是正确的，但是文章内容一个都点不开……遂决定推倒重来
{{< /tab-panel >}}
{{< /tab-view >}}

{{< hr "到这里就完成了博客的搭建和部署！" >}}
## 博客维护与完善
### 1. 如何更新博客
### 2. 免费域名获取及重定向
### 3. 其他可能有用的
{{< accordion "记在这里以备不时之需。" close >}}
- [Luna支持的美丽短代码](https://hugo-theme-luna.imiku.me/zh-cn/2022/05/02/shortcodes.html/)
{{< /accordion >}}
  


