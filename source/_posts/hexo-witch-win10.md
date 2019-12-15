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

5. hexo deploy失败

   ​	问题现象：

   ```
   PS D:\Blog>  hexo deploy
   INFO  Deploying: git
   INFO  Clearing .deploy_git folder...
   INFO  Copying files from public folder...
   INFO  Copying files from extend dirs...
   fatal: in unpopulated submodule '.deploy_git'
   FATAL Something's wrong. Maybe you can find the solution here: https://hexo.io/docs/troubleshooting.html
   Error: Spawn failed
       at ChildProcess.<anonymous> (D:\Blog\node_modules\hexo-util\lib\spawn.js:52:19)
       at ChildProcess.emit (events.js:210:5)
       at ChildProcess.cp.emit (D:\Blog\node_modules\cross-spawn\lib\enoent.js:40:29)
       at Process.ChildProcess._handle.onexit (internal/child_process.js:272:12)
   ```

   ​	解决方法： 删除./.deploy_git 文件夹。然后重新deploy

6. hexo backup失败

   PS D:\Blog> git push -u origin master 方式。

   

   

   

    