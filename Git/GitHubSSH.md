+++
Categories = ["Git","GitHub"]
author = "sincerelywy"
comments = true
date = "2016-01-23T23:06:00+08:00"
draft = false
image = ""
menu = ""
share = true
slug = "github-ssh"
tags = ["git","github"]
title = "GitHub使用SSH方式访问"

+++

# GitHub 使用 SSH 方式访问

日常使用中，安全的方式是使用HTTPS方式clone，并使用密码访问GitHub的个人Repo。但是在自己电脑上一遍遍的输密码也是很费事的，因此可以换为使用SSH方式。同时对于已经使用HTTPS方式clone的仓库，还可以使用git命令修改成git方式clone，这样在push的时候就能够使用SSH方式了。

<!--more-->

## 1. 使用SSH密钥

在Windows上，默认安装的Git客户端就能够生成SSH密钥。输入`ssh-keygen -t rsa -C "Ciphertext"`，按照步骤填写对应的内容，或者按回车直接默认生成。

然后将生成的`id_rsa.pub`内容增加到个人的https://github.com/settings/ssh，然后使用`ssh git@github.com`测试是否成功即可。我的输出内容如下：

```
Hi sincerelywy! You've successfully authenticated, but GitHub does not provide shell access.
```

成功后就可以在GitHub中选择git方式进行Clone。

## 2. 将Clone的Repo由HTTPS修改为SSH

这个只需要Git的一句命令即可完成。`git remote set-url origin git@github.com:someaccount/someproject.git`，origin后面是目标Repo。