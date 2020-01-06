.. vim: syntax=rst


NFS服务器环境搭建
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

虚拟机默认已经设置NFS服务器，默认服务器目录是

.. code-block:: sh
   :emphasize-lines: 2
   :linenos:

    /home/book/nfs_rootfs

用户如果需要自己搭建NFS环境请执行以下操作

1.安装nfs服务器：

.. code-block:: sh
   :emphasize-lines: 2
   :linenos:

    sudo apt-get install nfs-kernel-server

2.配置nfs服务器

.. code-block:: sh
   :emphasize-lines: 2
   :linenos:

    sudo vim /etc/exports
    //修改内容如下：
	    /home/book/nfs_rootfs *(rw,nohide,insecure,no_subtree_check,async,no_root_squash)

3.重启nfs服务:

.. code-block:: sh
   :emphasize-lines: 2
   :linenos:

    sudo service nfs-kernel-server restart

4.验证nfs服务器

.. code-block:: sh
   :emphasize-lines: 2
   :linenos:

    sudo mount -t nfs 192.168.2.101:/home/book/nfs_rootfs /mnt

5.开发板内核启动后挂根网络文件夹

.. code-block:: sh
   :emphasize-lines: 2
   :linenos:

    mount -t nfs  192.168.2.101:/home/book/nfs_rootfs /mnt
