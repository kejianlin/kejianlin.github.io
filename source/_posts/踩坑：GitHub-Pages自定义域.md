---
title: 踩坑：GitHub Pages自定义域
date: 2023-12-20 15:49:04
tags:
---

### 问题
之前我在GitHub Pages部署博客设置自定义域为kejianlin.top，最近部署网站导航新项目到GitHub Pages自动生成项目地址是kejianlin.top/ptsd，但是我希望是域名是ptsd.kejianlin.top。然后我在腾讯云进行域名解析将ptsd子域重定向到原始域，我错误以为原始域是kejianlin.top/ptsd，但是腾讯云报错CNAME 记录的指向字段只能填写目标域名而不能包含路径。
<!-- more -->


### 解决
在网站导航新项目GitHub Pages设置自定义域为ptsd.kejianlin.top，在腾讯云域名解析时设置子域name为ptsd，类型为CNAME，原始域改成是kejianlin.github.io。通过域名ptsd.kejianlin.top直接访问新项目网站导航。

### 总结
设置自定义域ptsd.kejianlin.top后，GitHub Pages 会根据在 GitHub 设置自定义域来匹配并正确显示项目kejianlin.github.io/ptsd。
