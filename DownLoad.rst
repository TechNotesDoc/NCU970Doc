.. vim: syntax=rst

资源下载
~~~~~~~~~~~~~~~

镜像文件和VMware下载
------------------------------------

1.下载ubuntu18.04 镜像文件: https://pan.baidu.com/s/1yG38CA_vOUQCUc1oNf8yQw  提取码：7p5u

2.安装VMware® Workstation 15 Pro，该软件牵扯版权问题，请用户自行下载安装

虚拟机打开镜像文件
------------------------------------
1.用VMware® Workstation 15 Pro打开ubuntu18.04的镜像文件；

 .. image:: ./media/01.虚拟机打开镜像文件.png
    :align: center

 .. image:: ./media/02.开启虚拟机.png
    :align: center

2.输入密码123456，开机即可。

 .. image:: ./media/03.输入密码.png
    :align: center
 
目录结构介绍
~~~~~~~~~~~~~~~
 /home/book 目录主要有nfs_rootfs、tftpboot、NUC970三个文件夹，功能如图所示。

 .. image:: ./media/04.目录结构.png
    :align: center

GitHub资源介绍
~~~~~~~~~~~~~~~

/home/book/NUC970目录下源码托管在gitHub，用户可以自己fork到自己的厂库clone到本地。具体git仓库地址如下：

1.uboot源码地址：https://github.com/Nuc970/uboot.git

2.Linux内核源码地址：https://github.com/Nuc970/NUC970_Linux_Kernel.git

3.文件系统地址：https://github.com/Nuc970/rootfs.git
