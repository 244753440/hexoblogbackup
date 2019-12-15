---
title: Hexo在win10上应用
date: 2019-12-15 22:22:28
tags:
---



​	之前hexo是搭建在Linux环境下，最近重装了电脑和系统，切换至win10。在此记录一下使用过程中的问题。



1. 重新安装hexo

   1. 遇见了无法执行hexo server命令的情况，错误提示:

      ```
      hexo : 无法加载文件 C:\Users\Administrator\AppData\Roaming\npm\hexo.ps1，因为在此系统上禁止运行脚本。
      ```

      参考 https://blog.csdn.net/y_0232/article/details/102555209 解决。

2. 恢复之前的笔记

   1. 备份及恢复方法参考 https://lrscy.github.io/2018/01/26/Hexo-Github-Backup/ 。

3.  将文章上传github

   1.  安装deployer-git 

      ```
      npm install hexo-deployer-git --save
      ```

      然后修改 ./_config.yml中修改deploy属性 

4. 使用

   1.  生成新的文章

       hexo new post <title> 

   2. 命令

      ```bash
      hexo clean		清除之前生成结果
      hexo generate	重新生成静态文件
      hexo server		运行hexo服务器，一般是http://127.0.0.1:4000/
      hexo deploy		部署
      hexo backup		备份
      ```

   