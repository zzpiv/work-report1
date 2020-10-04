# work-report1
work report
2020.9.28

1. Download and install Arduino IDE, eagle and GitHub clients.

2 passed https://www.tinkercad.com/learn/project-gallery;collectionId=OMOZACHJ9IR8LRE The website has learned the programming format of Arduino, the use of common library of Arduino, code writing and online debugging. The program of lighting and flashing LED light, actuator driver and ultrasonic distance measurement program are compiled.

3. Learn the common functions of GitHub.


2020.9.28
	1.下载并安装了arduino IDE，EAGLE，github客户端。
	2通过https://www.tinkercad.com/learn/project-gallery;collectionId=OMOZACHJ9IR8LRE网站学习了arduino的编程格式，了解了arduino常用库的使用和代码编写，在线调试。编写了点亮并让LED灯闪烁程序，舵机驱动程序，超声波测距程序。
	3.学习了解github的常用功能。
	
2020.9.30
	1.月arduino与mpu6050进行连接，并使用驱动库对mpu6050获得的数据进行欧拉角的转换，在串口上显示姿态解算后的3个欧拉角的变化。
	
![image](https://github.com/zzpiv/work-report1/blob/master/images/3900UUYY.PNG)

Mpu6050代码：

#include "I2Cdev.h"

#include "MPU6050_6Axis_MotionApps20.h"

MPU6050 mpu;

uint8_t fifoBuffer[64];

Quaternion q;

VectorFloat gravity;    //

float ypr[3];           //姿态解算后存放欧拉角的数组

void setup()
{

  Serial.begin(115200);//设置串口波特率为115200
  
  mpu.initialize();     //以下为库函数的调月，对mpu6050进行初始化
  
  mpu.dmpInitialize();
  
  mpu.CalibrateAccel(6);
  
  mpu.CalibrateGyro(6);
  
  mpu.PrintActiveOffsets();
  
  mpu.setDMPEnabled(true);
  
}

void loop()

{

  if (mpu.dmpGetCurrentFIFOPacket(fifoBuffer))
  
  {
  
    mpu.dmpGetQuaternion(&q, fifoBuffer);
    
    mpu.dmpGetGravity(&gravity, &q);
    
    mpu.dmpGetYawPitchRoll(ypr, &q, &gravity);
    
    Serial.print("ypr\t");                //打印出xyz3个欧拉角数据
    
    Serial.print(ypr[0] * 180 / M_PI);
    
    Serial.print("\t");
    
    Serial.print(ypr[1] * 180 / M_PI);
    
    Serial.print("\t");
    
    Serial.println(ypr[2] * 180 / M_PI);
    
  }
  
}

3.用EAGLE练习画原理图和pcb图的布局布线。
![image](https://github.com/zzpiv/work-report1/blob/master/images/35D9E8F72C073E1226F4EB338871DA04.png)
	![image](https://raw.githubusercontent.com/zzpiv/work-report1/master/images/35D9E8F72C073E1226F4EB338871DA04.png)
	![image](https://github.com/zzpiv/work-report1/blob/master/images/5C0C920D160C0C358ADFFD7AA1E4E9AD.png)
