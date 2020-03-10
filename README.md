Dell OptiPlex 3050 OC EFI on Catalina(macOS 10.15.x)
----
### 基于OPenCore 0.5.6正式版，机型为Dell OptiPlex 3050，系统版本为Catalina 10.15.3 <br>

### 注意：config文件已剔除MLB、SN、UUID等信息，如需使用该文件请自行填补。<br>

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


### 正常功能：<br>
1、GPU视频硬解<br>
2、cpu变频<br>
3、扬声器(内置+耳机口)<br>
4、HDMI、DP<br>
5、USB3.0（未定制）<br>
6、外接USB3.0 Hub速率正常<br>
6、光驱<br>

### 不正常功能：<br>
1、睡眠 （未调整、公司电脑不方便测试）<br>
2、麦克风是否可用未知（无相关设备来测试）<br>

##### 公司电脑目前已满足正常工作和稳定性需求，其他无关功能测试修补不再做测试或更新，有兴趣的小伙伴可用尝试修复和定制接口


安装配置过程所使用资料均来自网络，包括但不限于以下：
[tonymacx86:Heporis](https://www.tonymacx86.com/threads/mojave-10-14-5-on-dell-optiplex-3050.279277/)<br>
[精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)<br>
[使用OpenCore引导黑苹果-xin's blog](https://blog.xjn819.com/?p=543)<br>
[OC-little](https://github.com/daliansky/OC-little)<br>
[OpenCore Vanilla Guide](https://khronokernel-2.gitbook.io/opencore-vanilla-desktop-guide/)

