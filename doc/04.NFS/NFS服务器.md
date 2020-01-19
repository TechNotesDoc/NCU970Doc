# NFS环境搭建

虚拟机默认已经设置NFS服务器，默认服务器目录是

```
/home/book/nfs_rootfs
```

用户如果需要自己搭建NFS环境请执行以下操作。

## 安装nfs服务器

```
sudo apt-get install nfs-kernel-server
```

## 配置nfs服务器

```
sudo vim /etc/exports 
//修改内容如下：         

/home/book/nfs_rootfs *(rw,nohide,insecure,no_subtree_check,async,no_root_squash)
```

## 验证nfs服务器

```
sudo mount -t nfs 192.168.2.101:/home/book/nfs_rootfs /mnt
```

## 开发板内核启动后挂根网络文件夹

```
mount -t nfs  192.168.2.101:/home/book/nfs_rootfs /mnt -o nolock
```

