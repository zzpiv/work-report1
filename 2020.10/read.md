# 2020.10.6

   学习microbit的图形化编程
   
    1.按下A键显示灯

![image](https://github.com/zzpiv/work-report1/blob/master/images/button.PNG)

![image](https://github.com/zzpiv/work-report1/blob/master/images/light.PNG)
   
![image](https://github.com/zzpiv/work-report1/blob/master/images/led.PNG)

   2.随机出石头剪刀布

![image](https://github.com/zzpiv/work-report1/blob/master/images/caiquan.PNG)

   3.超声波测距控制sg90舵机旋转一定角度
   
![image](https://github.com/zzpiv/work-report1/blob/master/images/sg90.PNG)

# 2020.10.13

  1.在使用EAGLE绘制原理图和pcb的过程中，发现EAGLE的官方库的封装较少，记录一下几个常用的封装库下载网站：
    
   www.kicad-pcb.org
    
   www.digikey.cn
    
   www.ultralibrarian.com
    
   www.samacsys.com

https://github.com/jkantarek/Eagle-Libraries
    
   2.经过两天的学习，绘制了EAGLE的原理图和pcb图。
   
  # 2020.10.23
  
  1.对有故障的主控板进行检测和故障排查，将故障原因标记出来，并拆板检查原因。
  
  2.安装vpn访问外国网站。
  
  3.
    
   ![image](https://github.com/zzpiv/work-report1/blob/master/images/sch.PNG)
   
   ![image](https://github.com/zzpiv/work-report1/blob/master/images/pcb.PNG)
   
   
# 2020.10.14
 
 1.今天按照microbit的BOM表格式整理了板子的BOM表。
 
 2.按照arduino原理图的格式修改了原先自己画的原理图。
 
 3.寻找元器件的3d模型。

# 2020.10.15

1.今天重新用EAGLE绘制了板子的原理图和pcb图。

2.更新电脑环境以安装fusion 360

3.了解了红外遥控芯片的工作原理，根据已经印制好的红外遥控pcb板用EAGLE来重新绘制其原理图

# 2020.10.16

1.经过对window系统的更新配置，成功安装了fusion360.

2.根据遥控器的pcb板绘制完成其电路原理图。

3.查找了低电压检测IC的相关资料。

# 2020.10.19

1.了解了cns2低电压检测ic的工作原理。

2.根据红外遥控pcb双面板徒手绘制其pcb图。

![image](https://github.com/zzpiv/work-report1/blob/master/images/hwpcb.jpg)

3.了解了常用电容电阻的封装尺寸。

贴片电容：0402、0603、0805、1206、1812、2010、2225、2512（英寸表示）04 表示长度是0.04 英寸，02 表示宽度0.02 英寸。

电容电阻外形尺寸与封装的对应关系是：

0402=1.0mmx0.5mm

0603=1.6mmx0.8mm

0805=2.0mmx1.2mm

1206=3.2mmx1.6mm

1210=3.2mmx2.5mm

1812=4.5mmx3.2mm

2225=5.6mmx6.5mm

贴片钽电容的封装是分为

A型（3216），

B型（3528），

C型（6032），

D型（7343），

E型（7845）。有斜角的是表示正极


# 2020。10.20

1.修改了红外遥控原理图不规范的地方。

2.查找了红外遥控原理图中每一个元件的datasheet。

3.修改了红外IC的封装和低电压检测IC的封装。

4.上传yaokong20201020.zip，包含了原理图，datasheet，library。

记录一个eda网站：https://easyeda.com/

# 2020.10.21 

&emsp;1.根据microphone的pcb板，通过万用表检测各个元器件的属性值和网络连线，绘制其[电路原理图](https://github.com/zzpiv/work-report1/tree/master/EI09-04/LAYOUT)

&emsp;2.查找microphone模块上所用到的元器件[datasheet](https://github.com/zzpiv/work-report1/tree/master/EI09-04/datasheet)

&emsp;3.根据microbitBOM表格式重新整理了microphone模块的[BOM表](https://github.com/zzpiv/work-report1/tree/master/EI09-04/BOM)。

&emsp;4.整理好microphone的电路原理图，BOM表，datasheet资料并上传。

# 2020.10.22
&emsp; 1.根据麦克风模块pcb的实际尺寸一模一样的进行pcb layout。    
&emsp; 2.完全根据microbit的BOM表格式对昨天整理的麦克风BOM表进行修改，修改了P/N，description,manufacturer.  
&emsp; 3.在这个网站学习了解常用电容电阻三极管IC的封装尺寸。https://www.electronics-notes.com/articles/electronic_components/surface-mount-technology-smd-smt/packages.php

 #### COMMON SMD TANATALUM CAPACITOR PACKAGE DETAILS
  
| SMD PACKAGE TYPE	|  DIMENSIONS MM	       |   EIA STANDARD    |
| --------           | -----:                 | :----:            |
| Size A	            |   3.2 x 1.6 x 1.6	    |     EIA 3216-18   |
| Size B	            |   3.5 x 2.8 x 1.9	    |    EIA 3528-21    |
| Size C	            |   6.0 x 3.2 x 2.2	    |   EIA 6032-28     |
| Size D	            |   7.3 x 4.3 x 2.4	    |      EIA 7343-31  |
| Size E	            |   7.3 x 4.3 x 4.1	    |   EIA 7343-43     |

#### Transistor & diode packages

+ SOT-23 - Small Outline Transistor:size:3 mm x 1.75 mm x 1.3 mm。

+ SOT-223 - Small Outline Transistor:size:6.7 mm x 3.7 mm x 1.8 mm

#### Integrated circuit SMD packages

+ TSOP - Thin Small Outline Package:   This surface mount IC package is thinner than the SOIC and has a smaller pin spacing of 0.5 mm
+ SSOP - Shrink Small Outline Package:   This package has a pin spacing of 0.635 mm
+ TSSOP - Thin Shrink Small Outline Package:  
+ QSOP - Quarter-size Small Outline Package:   It has a pin spacing of 0.635 mm
+ VSOP - Very Small Outline Package:   This is smaller than the QSOP and has pin spacing of 0.4, 0.5, or 0.65 mm.


# 2020.10.23

1.安装vpn来访问外国网站

2.检查测试有故障的EQ_DUINO主控板的故障原因，并记录下来，对生锈的弹簧进行更换，拆板进行维修。

3.测试时主要检查板子能否烧录程序，如果不能就是ISP问题，可以下载程序但是电机通电不动就是驱动芯片问题或者是电源IC出现故障，更换电源IC即可。








