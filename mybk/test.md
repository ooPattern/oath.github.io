---
title: 如何优雅的使用typora
date: 2017-05-21 21:31:03
tags:
---

#### 环境搭建部署

##### 软件安装

注意：Node.js > 表示Node.js命令行，git > 表示git命令行。

1）git，git命令行，发布上传到github

2）Node.js，hexo工具依赖，windows选择32bit或64bit安装。

3）Node.js > npm install -g hexo-cli，安装hexo客户端。

4）git > hexo init blog，初始化目录，存放博客md文件。

5）Node.js > npm install。

6）Node.js > npm install hexo-deployer-git -S

7）Node.js > npm install hexo-asset-image --save

<!-- more -->

##### Github设置

1）创建一个新的repository：你的Github用户名.github.io

2）确认用户名必须一致，否则浏览器访问博客的时候会出现404错误。

 ![gitname](/img/gitname.png)

3）设置Github的SSH。开发者向GitHub版本库写入最常用到的协议是SSH协议，因为SSH协议使用公钥认证。

git > ssh-keygen -t rsa -C  "Github的注册邮箱地址"

git > ssh add xxxx

git > cd C:\Users\Administrator\.ssh\; vim id_rsa.pub

进入 https://github.com/settings/ssh 将rsa内容填写到key中。

##### 配置hexo

1）目录结构，md文件放到source文件夹，图片放到public/img文件夹。

 ![hexodir](/img/hexodir.png)

2）修改配置文件_config.yml

具体配置选项可参考github.io项目的_config.yml文件。

**注意**：每一项的填写，其`:`后面都要保留一个空格。

3）运行hexo命令，上传github

hexo g # 生成静态HTML网页

hexo d #上传到github

hexo s # 本地调试，http://localhost:4000

##### 可视化编辑hexo

1）用Typora(Windows版本)编写博客，保存为.md后缀。

2）图片资源存放到public/img文件夹下。引用方法：/img/imgname.png

3）将md文件拷贝到source/__post/目录下，然后执行：

git > hexo g # 生成HTML网页

git > hexo d # 上传github

#### 如何优雅的使用typora

```c++
#include<stdio.h>
int main(void)
{
    printf("hello oopattern\n");
    return 0;
}
```

图片可以直接拖拽进来~  ![jieping](/img/jieping.png)



