# OptiPlex-3050-OC-EFI
Dell OptiPlex 3050 OC EFI on Catalina(macOS 10.15.x)

基于最新OPenCore 0.5.6正式版配置，使用机型为Dell OptiPlex 3050，安装系统版本为Catalina 10.15.3

注意：config文件已剔除MLB、SN、UUID等信息，如需使用该文件请自行填补。
-----------------------------
具体配置如下：
CPU：i5 7400
RAM：8G DDR4 （single）
GPU：HD630 （only）
Disk：128G SSD（sata）+1T HDD
-----------------------------------

###注意：由于dell机型的特殊性，使用前需要先进行如下操作修改BIOS：
1、将U盘格式化为fat32，将GRUB文件夹下"EFI.zip"解压将到U盘根目录
2、开机时按F12选择从U盘启动，进入GRUB界面：
3、在GRUB界面中输入：
      setup_var 0x795 0x2 回车（修改dvmt为64MB）
      setup_var 0x4ed 0x0 回车（关闭CFG）

##方法来源：https://www.tonymacx86.com/threads/mojave-10-14-5-on-dell-optiplex-3050.279277/   ###


正常功能：
1、GPU视频硬解
2、cpu变频
3、扬声器(内置+耳机口)
4、HDMI、DP
5、USB3.0（未定制）
6、外接USB3.0 Hub速率正常
6、光驱

不正常功能：
1、睡眠 （未调整、公司电脑不方便测试）
2、麦克风是否可用未知（无相关设备来测试）

公司电脑目前已满足正常工作和稳定性需求，其他无关功能测试修补不再做测试或更新，有兴趣的小伙伴可用尝试修复和定制接口
