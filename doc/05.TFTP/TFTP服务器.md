# TFTP服务器环境搭建

虚拟机默认已经设置TFTP服务器，默认服务器目录是

```
/home/book/tftpboot
```

用户如果需要自己搭建TFTP环境请执行以下操作.

## 安装tftp服务器

```
sudo apt-get install tftp-hpa tftpd-hpa 
```

## 配置tftp服务器

```
mkdir -p /home/book/tftpboot chmod 777 /home/book/tftpboot 
sudo vim /etc/default/tftpd-hpa
//修改内容如下：
TFTP_DIRECTORY="/home/book/tftpboot"   TFTP_OPTIONS="-l -c -s"
```

## 重启TFTP服务

```
sudo service tftpd-hpa restart
```

## 验证TFTP

```
tftp 192.168.2.147 tftp> get b.txt tftp> q ls b.txt
```

