---
title: SSH
icon: ssh
time: '2019-11-23T00:00:00.000Z'
category: Linux
tag:
  - SSH
---

# ssh

## 使用密码登录

1. 执行以下命令，连接 Linux 云服务器。

   ```bash
   ssh <username>@<hostname or IP address>
   ```

   * username 即为前提条件中获得的默认帐号。
   * hostname or IP address 为您的 Linux 实例公网 IP 或自定义域名。

2. 输入已获取的密码，按 Enter，即可完成登录。

## 使用密钥登录

1. 执行以下命令，赋予私钥文件仅本人可读权限。

   ```text
   chmod 400 <下载的与云服务器关联的私钥的绝对路径>
   ```

2. 执行以下命令，进行远程登录。

   ```text
   ssh -i <下载的与云服务器关联的私钥的绝对路径> <username>@<hostname or IP address>
   ```

   * username 即为前提条件中获得的默认帐号。
   * hostname or IP address 为您的 Linux 实例公网 IP 或自定义域名。

   例如，执行 `ssh -i "id_rsa" ubuntu@123.206.113.227` 命令，远程登录 Linux 云服务器。

## 断开链接

`Ctrl + D` 或 输入 `logout`.

