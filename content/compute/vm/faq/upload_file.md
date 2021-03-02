---

title: "怎样将文件上传到云服务器"
date: 2020-01-30T00:38:25+09:00
description: Test description
weight: 40
draft: false
enableToc: false
---

**本地Windows主机通过MSTSC上传文件到Windows云服务器**

**操作场景**

将文件上传至Windows云服务器一般会采用MSTSC远程桌面连接的方式。本节为您介绍本地Windows计算机通过远程桌面连接，上传文件至Windows云服务器的操作方法。

**前提条件**

Windows云服务器可以访问公网

**操作步骤**

1、在电脑桌面中使用“WIN＋R”组合键，打开“运行”窗口，输入“mstsc”命令并回车即可弹出远程桌面连接对话框。

2、单击"显示选项"。

<img src="../../_images/upload_file_01.png" width="60%" height="40%">

<p></p>

3、在“常规”页签中，输入云服务器的公网IP地址和用户名“Administrator”。

<img src="../../_images/upload_file_02.png" width="60%" height="40%">

<p></p>

4、选择“本地资源”页签，确认“本地设备和资源”下的“剪切板”处于勾选状态。

<p></p>

<img src="../../_images/upload_file_03.png" width="60%" height="40%">

<p></p>

5、单击"详细信息"。

<p></p>

6、在“驱动器”多选框列表，勾选要上传到Windows云服务器上的文件所在的本地磁盘。

<p></p>

<img src="../../_images/upload_file_04.png" width="60%" height="40%">

<p></p>

7、点击“确定”，登录Window云服务器。

<p></p>

8、单击“开始 > 计算机”。
      在出现的Windows云服务器上可看到本地硬盘的信息。

<p></p>

9、在云服务器中，双击进入本地磁盘，将需要上传的文件复制到Windows云服务器。

<p></p>

**本地Windows主机使用WinSCP上传文件到Linux云服务器**

**操作场景**

WinSCP工具可以实现在本地与远程计算机之间安全地复制文件。通过 WinSCP 可以直接使用服务器账户密码访问服务器，无需在服务器端做任何配置。
通常本地Windows计算机将文件上传至Linux服务器一般会采用WinSCP工具。本节为您介绍本地Windows计算机使用WinSCP工具，上传文件至Linux云服务器的操作方法。本例中云服务器操作系统为CentOS。

**操作步骤**

1、下载 WinSCP 客户端并安装。<a href="https://winscp.net/" target="_blank">下载WinSCP</a>

<p></p>

2、安装WinSCP。

<p></p>

3、启动WinSCP，启动后界面如下：

<p></p>

<img src="../../_images/upload_file_05.png" width="60%" height="40%">

<p></p>

填写说明：

- 协议：选填 SFTP 或者 SCP 均可。
- 主机名：云服务器的公网 IP。登录管理控制台即可查看对应云服务器的公网 IP。
- 端口：默认 22。
- 用户名：云服务器的用户名。
- 密码：购买云服务器设置的密码。

1. 单击“登录”，进入 “WinSCP” 文件传输界面。

2. 登录成功之后，您可以选择左侧本地计算机的文件，拖拽到右侧的远程云服务器，完成文件上传到云服务器。

   <p></p>

   

**本地Linux主机使用SCP上传文件到Linux云服务器**

<p></p>

**操作场景**

本节介绍本地Linux主机通过SCP向Linux云服务器传输文件的操作步骤。

**操作步骤**

**上传文件**

在本地Linux操作系统主机上执行以下命令，传输文件到Linux操作系统云服务器。

```
scp 本地主机文件地址 用户名@弹性公网IP:云服务器文件地址

例如：将本地文件 /test.txt 上传至弹性公网IP地址为139.198.x.x的云服务器对应目录下，命令如下：

scp /test.txt root@139.198.x.x:/home

根据提示输入登录密码，即可完成上传。
```

**下载文件**

在本地Linux操作系统主机上执行以下命令，下载云服务器上的文件到本地主机。

```
scp 用户名@弹性公网IP:云服务器文件地址 本地主机文件地址

例如，将弹性公网IP地址为139.198.x.x的云服务器文件/test.txt 下载至本地对应目录下，命令如下：

scp root@139.198.x.x:/test.txt /home

根据提示输入登录密码，即可完成文件下载。
```

<p></p>
