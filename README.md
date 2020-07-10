---
title: Jenkins+TestNG搭建自动化测试平台
date: 2020-05-12 15:51:49
updated: 2020-05-12 16:00:00
tags: [docker,软件测试]
categories: [软件测试]
---

# 使用docker安装

## 先拉取镜像

```bash
docker pull jenkins/jenkins
```

## 运行镜像

### 先建立文件夹

```bash
mkdir /home/Xhofe/Jenkins
```

### 设置文件夹成员组

```bash
sudo chown 1000:1000 /home/Xhofe/Jenkins
```

### run

```bash
docker run -itd --privileged=true -v /home/Xhofe/Jenkins:/var/jenkins_home -p 8080:8080 -p 50000:50000 jenkins/jenkins
```

### 完成

现在就可以访问`ip`/域名:8080进行进一步的设定了。密码在`/home/Xhofe/Jenkinssecrets/initialAdminPassword`。
