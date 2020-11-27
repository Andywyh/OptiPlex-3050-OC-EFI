Dell OptiPlex 3050 OC EFI on Catalina(macOS 11.0.1)
----
### 基于OPenCore 0.6.3正式版，机型为Dell OptiPlex 3050，系统版本为Big Sur 11.01 ，机型iMac 18,1<br>

### 注意：config文件中MLB、SN、UUID等机型信息请自行更改后使用。<br>
================================================================================================<br>
### 具体配置如下：<br>
CPU：i5 7400 <br>
RAM：8G DDR4 （single）<br>
GPU：HD630 （only）<br>
Disk：128G SSD（sata）+1T HDD  <br>

### 注意：由于dell机型的特殊性，使用前需要先进行如下操作修改BIOS：<br>
1、将U盘格式化为fat32，将GRUB文件夹下"EFI.zip"解压将到U盘根目录 <br>
2、开机时按F12选择从U盘启动，进入GRUB界面： <br>
3、在GRUB界面中输入： <br>
      setup_var 0x795 0x2 回车（修改dvmt为64MB）<br>
      setup_var 0x4ed 0x0 回车（关闭CFG)<br>

<方法来源：https://www.tonymacx86.com/threads/mojave-10-14-5-on-dell-optiplex-3050.279277/  > <br>
================================================================================================<br>

### 正常功能：<br>
1、GPU视频硬解<br>
2、cpu变频<br>
3、声卡（ALC255，layout ID 11）<br>
4、HDMI、DP<br>
5、USB3.0（未定制）<br>
6、外接USB3.0 Hub速率正常<br>
7、光驱<br>
8、网卡<br>
### 不正常功能：<br>
1、睡眠 <br>
================================================================================================<br>
##### 主机前面板二合一耳机插孔使用说明：<br>
---来源：[hackintosh-stuff/ComboJack](https://github.com/hackintosh-stuff/ComboJack)---<br>
1. 下载项目中ComboJack.zip文件并解压<br>
2. 打开终端，将ComboJack_Installer文件夹中的install.sh拖进终端窗口运行，运行完毕后重启<br>
3. 插入耳机的时候，会弹出对话框询问你插入的是耳机(headphones)还是耳麦(headset)或输入线路（line-in）<br>

##### 公司电脑目前已满足正常工作和稳定性需求，USB定制和睡眠修正不再做测试或更新，有兴趣的小伙伴可用尝试修复和定制接口<br>
================================================================================================<br>
#### 系统信息展示：
![image](https://github.com/Andywyh/OptiPlex-3050-OC-EFI/blob/master/Photos/cpu_info.png?raw=true)
![image](https://github.com/Andywyh/OptiPlex-3050-OC-EFI/blob/master/Photos/info.png?raw=true)
![image](https://github.com/Andywyh/OptiPlex-3050-OC-EFI/blob/master/Photos/Audio_info.png?raw=true)
![image](https://github.com/Andywyh/OptiPlex-3050-OC-EFI/blob/master/Photos/USB_info.png?raw=true)
================================================================================================<br>



安装配置过程所使用资料均来自网络，包括但不限于以下：<br>
[tonymacx86:Heporis](https://www.tonymacx86.com/threads/mojave-10-14-5-on-dell-optiplex-3050.279277/)<br>
[精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)<br>
[使用OpenCore引导黑苹果-xin's blog](https://blog.xjn819.com/?p=543)<br>
[OC-little](https://github.com/daliansky/OC-little)<br>
[OpenCore Vanilla Guide](https://khronokernel-2.gitbook.io/opencore-vanilla-desktop-guide/)<br>
[远景论坛](http://bbs.pcbeta.com/)<br>

