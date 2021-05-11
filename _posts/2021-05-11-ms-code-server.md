---
layout: post
title: "code-server使用教程"
date:  2021-05-08 20:33:01 +0800
categories: document
tag: 教程
---

* content
{:toc}
# 本文目的

**code-server**是vscode推出的服务器版本，可以通过将其部署在服务器中之后实现远程访问。可以在ipad等客户端或者是浏览器中实现使用vscode的效果。

# 参考资料

[【CSDN】服务器搭建code-server服务](https://blog.csdn.net/Xiudadasnb/article/details/107019039?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-2.control)

[【CSDN】在ipad上用Vscode](https://blog.csdn.net/weixin_43988498/article/details/110305091)

# 配置流程

1. 在服务器上下载并解压对应的code-server源码

   [【github】cdr发布地址](https://github.com/cdr/code-server/releases)

   ```bash
   # 下载安装包
   wget https://github.com/cdr/code-server/releases/download/v3.10.0/code-server-3.10.0-linux-amd64.tar.gz
   
   # 解压
   tar -xvzf code-server-3.10.0-linux-amd64.tar.gz
   
   # 重命名&移动到想要的位置
   mv code-server-3.10.0-linux-amd64 code-server
   ```

2. 运行code-server服务

   - 直接运行`code-server`服务会产生如下报错

     ```bash
     ***** Please use the script in bin/code-server instead!
     ***** This script will soon be removed!
     ***** See the release notes at https://github.com/cdr/code-server/releases/tag/v3.4.0
     [2021-05-11T15:10:10.883Z] error Please specify at least one file or folder
     ```

   - 改为使用`bin`文件夹中的程序，**注意：这里不能使用vscode的remote插件操作，否则会报错，要使用其他的SSH工具**

   - 需要管理员权限，运行程序

     `sudo ./code-server`

3. 可修改配置配置文件，位置在`~./config/code-server.yaml`

## 效果

网页端效果如下

![image-20210512000744537](https://i.loli.net/2021/05/12/fdehk4yYajbRscA.png)