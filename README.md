# 16x40像素点的WiFi网络点阵时钟

这是一个用ESP8266制作的WiFi网络时钟，主要功能是获取网络上的时间并显示在16x40像素的点阵屏幕上。除了显示网络时间外，还可以通过Qt编写的上位机软件，设置计时、倒计时的功能，还能将文字和图片转成16x16像素大小显示出来，可以设置汉字滚动，类似于广告牌的效果。设置有两种供电方式，type-C供电和电池供电，也支持电池充电。当插入type-C线后，会自动切换至type-C供电，当拔出type-C后自动切换为电池供电。



**视频演示效果**

【【开源】使用ESP8266单片机自制一个WiFi网络时钟】 https://www.bilibili.com/video/BV1ih4y1B7jL/?share_source=copy_web&vd_source=3b521714205edc9e868eb79d7cf2244a



### 目前做了一下几个功能：

1. 网络时钟
2. 计时显示
3. 倒计时显示
4. 静态显示（显示16x16像素图片或者文字）
5. 汉字滚动显示



### 关于制作：

成本低廉，仅需42元，采用0603的电阻，焊接相对简单一些。

已将所需的元件的购买连接整理成BOM表。电子元件已经尽量选择在同一家购买了，但是难免会遇到有些没有的情况，这里选择分开购买，大概有三四家店左右，所以不会收到很多快递。如有疏漏，请指正！

电池和PCB打样的成本不计算在里面，电池可以单独购买，大小不超过50x50mm就行，电池的正负极不要搞错了，不然可能会烧坏芯片。

可以买一块2mm厚的黑色透明的亚克力板作为挡板放到点阵屏幕面前，尺寸是100mmx54mm，这样可能看起来会没那么刺眼。如果加了挡板，需要用M3x13mm的铜柱4颗，M3x12mm的螺丝4颗和M3x6mm的螺丝4颗用于固定挡板。

还有，挡板的孔要自己打。挡板很便宜，两三块钱就行了，淘宝找一家可以帮忙切割的，就不用自己切割了，买回来打孔就行，如果要卖家帮忙打孔，可能要另外收费了。

 

代码编译：由于使用Arduino进行编程，需要将代码用ArduinoIDE打开，编译后上传至ESP8266即可。（我这里用的ArduinoIDE是1.8版本的）

WiFi配网：首次使用，需要用手机打开设置，连接WiFi名为ESP8266-NTP-CLOCK的网络，然后打开浏览器，输入192.168.4.1，进去网页之后，再输入自己路由器的名称和密码，名称要用英文，不然可能会连不上。



**网络时钟的显示效果：**

![image-20231008162616.png](https://github.com/literem/desktop-matrix-clock/blob/main/3.%E5%9B%BE%E7%89%87/20231008162616.png?raw=true)

![image-20231008162755.png](https://github.com/literem/desktop-matrix-clock/blob/main/3.%E5%9B%BE%E7%89%87/20231008162755.png?raw=true)

**还可以滚动显示**
![image-20231008162705.png](https://github.com/literem/desktop-matrix-clock/blob/main/3.%E5%9B%BE%E7%89%87/20231008162705.png?raw=true)

**焊接后的实物图：**
![image-20231008164931.png](https://github.com/literem/desktop-matrix-clock/blob/main/3.%E5%9B%BE%E7%89%87/20231008164931.png?raw=true)

![image-20231008165046.png](https://github.com/literem/desktop-matrix-clock/blob/main/3.%E5%9B%BE%E7%89%87/20231008165046.png?raw=true)

![image-20231008165026.png](https://github.com/literem/desktop-matrix-clock/blob/main/3.%E5%9B%BE%E7%89%87/20231008165026.png?raw=true)

![image-20231008164953.png](https://github.com/literem/desktop-matrix-clock/blob/main/3.%E5%9B%BE%E7%89%87/20231008164953.png?raw=true)
