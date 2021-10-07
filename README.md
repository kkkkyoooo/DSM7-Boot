# Synology7-Boot


#### 适用于PVE虚拟机的黑群晖7.x的引导镜像



* 常规创建一个PVE虚拟机，创建完成后，别开机，登录PVE的SSH：

```
vi /etc/pve/qemu-server/102.conf
```
ps：102 为群晖虚拟机ID，根据实际情况更改

添加下面的一长串代码：

```
args: -device 'qemu-xhci,addr=0x18' -drive 'id=synoboot,file=/root/synoboot7.img,if=none,format=raw' -device 'usb-storage,id=synoboot,drive=synoboot,bootindex=5'
```

* /root/synoboot7.img  在root目录下放群晖引导镜像

* 回到PVE，添加SATA的硬盘，并添加3个串口，启动DSM7

ps：现在来说，串口可添加，可不添加

* 输入网址 http://find.synology.cn/ 查找设备

