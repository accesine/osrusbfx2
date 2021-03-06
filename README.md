#osrusbfx2

Based on "OSRFX2 Learning Kit" + "CY001 learning Kit", added more with my idea to demo how-to learning writing host drivers for USB devices on Windows & Linux.

# 为何要写这个东东  
诸位学习主机（host）侧USB驱动开发的同仁，想必在学习过程中一定也有鄙人相同的经历感受。那就是手头如果有一块USB的开发学习板，那效率一定会高很多。所以在下当时也是出于此目的在网上买了张佩大侠提供的配合《竹林蹊径：深入浅出windows驱动开发》的学习板CY001，以作学习的用途。

我对驱动的学习是从Wiindows平台开始的，毕竟PC上Windows仍是霸主。在学习USB驱动开发时鄙人有一个重要的体会是：微软WDK中提供的例子是最值得仔细研习的。USB驱动相关的例子中尤以osrusbfx2这个例子最为经典。osrusbfx2是配合著名的OSRFX2学习板精心编写的一套例子。非常适合Windows上学习USB驱动开发的朋友入门学习用。不光是入门用，平时也会常常参考。据说微软WDK开发小组的程序员也要经常用OSRFX2的板子来做测试呢（具体在哪里看到的忘记了），可见其重要性。

接下来，众所周知的原因，对于中国大陆的程序员来说OSR的那块板子是在是贵了点。所以我手上有了CY001之后就有了个想法：能不能将CY001改造一下，模拟成OSRFX2呢。它们两的物理基础实际上相差并不大啊。

再接下来就有了这个项目。所以如果你手头有CY001，又想学习WDK的OSRUSBFX2例子，那不妨试试阅读以下我写的这个玩意。其实在设备（Device）侧，如果你没有CY001，但只要有任何一块基于Cypress的FX2系列USB芯片的学习开发板（大陆做这种开发板的貌似不少，淘宝上可以搜搜），同时你对修改设备的固件也有兴趣，都可以按照相同的思路尝试以下。我的这个就当是抛砖引玉了吧。

其实OSRUSBFX2这个例子对在Windows平台以外的系统上学习USB驱动开发也是很有帮助的，以Linux为例，一样的受用。而且在Windows上学好USB驱动开发后再回过头去看Linux上的USB驱动开发，也是大有裨益。毕竟微软人家也是USB协议的主要发起者之一啊。

# 目录结构  
+ osrfx2fw - CY001的固件Keil工程源代码。已经过修改模拟OSRFX2学习板  
 - [README](./osrfx2fw/README.md): 介绍了如何基于CY001模拟OSRFX2。  
+ windows  - Windows版本的源代码和相关文件。已经过修改以适配CY001与实际的OSRFX2学习板的不同。  
 - drivers - 驱动安装包。目前只提供了x86的版本。  
      * [README](./windows/drivers/README.md)  
 - drvinst - 驱动安装和卸载程序，演示DIFxAPI和SetupAPI的典型用例。  
      * [README](./windows/drvinst/README.md)  
      * [(原创)Windows设备和驱动的安装](./windows/drvinst/device-and-driver-installation.md)  
 - osrusbfx2 - WDK的osrusbfx2例子，经过修改适配CY001。  
      * [README](./windows/osrusbfx2/README.md)  
      * [(原创)学习笔记-Developing Drivers with the Microsoft Windows Driver Foundation](./windows/osrusbfx2/doc/note-DDMWDF.md)  
      * [(原创)Step by Step, 为OSRFX2创建一个KMDF驱动程序](./windows/osrusbfx2/doc/Building-KMDF-Driver-for-OSRFX2.md): 一个基于osrusbfx2例子的小教程。  
+ linux - Linux版本的源代码和相关文件。  
 - [README](./linux/README.md)  
 - [(原创)学习笔记-Linux Device Drivers, 3rd Edition](./linux/doc/learning-ldd3/notes.md)  

更详细的说明可以参考各分目录下的说明文件。  

# 联系方式  
unicorn_wang@outlook.com


# 下载和访问  
该项目的所有文档和代码都上传到GitHub，大家如果熟悉GitHub可以上Github观赏并联机提出宝贵意见。地址是: https://github.com/unicornx/osrusbfx2

下载该项目的方法：

mkdir yourworkspacefolder  
cd yourworkspacefolder  
git clone https://github.com/unicornx/osrusbfx2.git

该项目另一个发布的平台在“图灵社区” - "osrusbfx2 - Step by Step USB驱动开发"  
http://www.ituring.com.cn/minibook/726

enjoy it! :)

    
      


