VMWare虚拟机安装VMware Tools

![img](https://gitee.com/lichaikui/picture/raw/master/tupian/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xja2luZzE4MzI1,size_16,color_FFFFFF,t_70.png)

打开虚拟机没有VMware Tools非常不方便，但是没设置好导致“重新安装VMware Tools”变成灰色，解决办法：
1、在设置中将以下三项设置为使用物理驱动器

![在这里插入图片描述](https://gitee.com/lichaikui/picture/raw/master/tupian/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xja2luZzE4MzI1,size_16,color_FFFFFF,t_70-16375933178022.png)

2、现在可以点击重新安装
3、可以看见出现了VMware Tools文件夹

![在这里插入图片描述](https://gitee.com/lichaikui/picture/raw/master/tupian/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xja2luZzE4MzI1,size_16,color_FFFFFF,t_70-16375933708564.png)

4、使用tar命令将压缩包解压到指定文件夹，注意不能直接解压到/media，因为该文件夹是只读

sudo tar zxvf VMwareTools-10.3.10-13959562.tar.gz -C /home

5、解压完成后，进入文件夹，执行vmware-install.pl文件

![在这里插入图片描述](https://gitee.com/lichaikui/picture/raw/master/tupian/20191126091326449.png)

安装命令：sudo ./vmware-install.pl

![在这里插入图片描述](https://gitee.com/lichaikui/picture/raw/master/tupian/20191126091519884.png)

6、安装完成后，重启虚拟机，验证是否安装成功：

将本机中的文件直接拖到虚拟机中，如果可以则安装成功
界面会铺满窗口，不再有黑边，单击虚拟机全屏按钮，如果铺满全屏，则安装成功
7、如果安装VMware Tools不行，推荐安装open-vm-tools
sudo apt-get autoremove open-vm-tools
sudo apt-get install open-vm-tools
sudo apt-get install open-vm-tools-desktop
------------------------------------------------

原文链接：https://blog.csdn.net/Lcking18325/article/details/103249783