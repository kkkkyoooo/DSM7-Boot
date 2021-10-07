# Synology7-Boot

#### 本镜像仅作测试之用，若您下载，请24小时内删除。

#### 本项目发布的镜像默认仅适合PVE！若是其他自行查询相关教程！

#### PVE虚拟机安装黑群晖7.x简单教程

* DS918+

* 常规创建一个PVE虚拟机，创建完成后，别开机，WinScp登录PVE；

* 上传引导镜像：/root/synoboot7.img；

* 登录到SSH终端，运行：(102为虚拟机ID，自行修改)
```
qm importdisk 102 synoboot7.img local-lvm
```

* 回到PVE，添加未使用的硬盘，设置为SATA的硬盘，并将此硬盘设置为第一启动；

* 启动DSM7，输入网址 http://find.synology.cn/ 查找设备

详细教程可参考[GXNAS保姆教程](https://wp.gxnas.com/11213.html)

