# 入门 

## 开发板使用 

1. 启动方式 

    - EMMC 启动 `0010` 
    - SD卡启动 `1110`
    - USB启动 `0001` 

## 环境搭建 

1. ubuntu主机安装nfs服务，开发板挂载
    - install `nfs server` 
        ```
        sudo apt-get install nfs-kernel-server 
        ```
    - configure `nfs server` 
        ```
        /home/victory/nfs_rootfs *(rw,nohide,insecure,async,no_subtree_check,no_root_squash)
        ```
    - client mount it 
        ```
        sudo mount -t nfs -o nolock,ver=3 10.10.18.17:/home/victory/nfs_rootfs ubuntu-host-dir/ 
        ```
