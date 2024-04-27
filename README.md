# esp8266_WI-PWN
>使用esp8266开发板烧录wifi攻击固件（WI-PWN）

# ESP8266---介绍
ESP8266是一款低成本、高性能的Wi-Fi模块，由乐鑫科技（Espressif Systems）开发。它集成了一颗32位的Tensilica处理器，具有Wi-Fi功能，能够通过串口与外部设备通信。以下是ESP8266的详细介绍：

## 1. 技术规格：
处理器： ESP8266模块通常配备Tensilica L106 32位微控制器，工作频率可达80MHz。
存储： 大多数ESP8266模块内置Flash存储器，用于存储程序和数据。常见容量为4MB。
通信： 支持802.11 b/g/n Wi-Fi标准，可作为站点（STA）或接入点（AP）运行。
接口： 通常具有多个GPIO（通用输入输出）引脚，SPI、I2C、UART等通信接口，以及模拟输入引脚。
电源： 通常工作电压为3.3V，但某些模块可以直接从5V供电。
## 2. 软件支持：
开发环境： 可以使用Arduino IDE、Espressif的ESP-IDF（ESP8266 IoT Development Framework）等开发环境进行编程。
编程语言： 支持C/C++编程。
库支持： 有丰富的库支持，包括Wi-Fi、TCP/IP、HTTP、MQTT等，方便快速开发各种应用。
## 3. 特性：
低成本： ESP8266是一款低成本的Wi-Fi模块，使得将Wi-Fi功能集成到各种设备中变得更加实惠。
灵活性： 可以通过软件配置实现多种Wi-Fi模式，如STA模式（连接到现有网络）和AP模式（创建自己的Wi-Fi网络）。
易用性： 通过简单的串口命令即可配置Wi-Fi连接，使得集成Wi-Fi功能变得相对简单。
社区支持： 有庞大的开发者社区支持，可以轻松获取教程、示例代码和技术支持。
## 4. 应用领域：
物联网（IoT）： ESP8266广泛应用于物联网设备，如智能家居、传感器节点、智能灯具等。
嵌入式系统： 由于其小巧的尺寸和强大的功能，ESP8266也被用于各种嵌入式系统中，如机器人、智能手表等。
远程控制： 可以利用ESP8266模块实现远程控制，如远程监控、远程操作等。
DIY项目： 由于易用性和低成本，ESP8266被广泛应用于各种DIY项目中，如智能家居控制、无线传感器网络等。

>总的来说，ESP8266是一款功能强大且易于使用的Wi-Fi模块，适用于各种物联网和嵌入式应用。



# ESP8266---材料准备
## 1.硬件设备
### 1.1（micro-usb）梯形安卓数据线（必须要可以传数据）
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/65c054ef4fbc4250975403aa29c623be.png)

### 1.2（ESP8266）
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/7c1f275977544231ac872486f1707661.png)


### 1.3（win电脑）（我记忆中手机也可以，但是找不到软件）
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/111caaa940e24e50866ff4d32eaffb71.png)

---
## 2.软件程序
### 2.1 程序分享
都是一样的文件，方便你们下载，本来想蓝奏云的不太会就懒弄了

```bash
GitHub：https://github.com/xk-mt/esp8266_WI-PWN

百度网盘：https://pan.baidu.com/s/1_YDOjfk8Gqm30l7ue7p1EQ?pwd=ABCD 提取码：ABCD

移动云盘：https://caiyun.139.com/m/i?185CEhzD0HREF 提取码:XuDj
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/6c0df16703e74242905d23bec6aa3ff3.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/8027d40483ae435b9135ef410233e5fd.jpeg)


### 2.2 驱动程序（CH341SER.EXE）
==所有的软件程序都分享在云盘提供学习下载==
下载官网：[CH341SER.EXE - 南京沁恒微电子股份有限公司](https://www.wch.cn/download/ch341ser_exe.html)
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/6c2eff97230642a98a06b304af2295f7.png)

### 2.3 烧录工具（分享了两个）

提供了两个烧录工具，ESP8266Flasher和flash_download_tool_3.9.6

==所有的软件程序都分享在云盘提供学习下载==
>下载官网：[GitHub nodemcu/nodemcu-flasher: A firmware Flash tool for nodemcu
](https://github.com/nodemcu/nodemcu-flasher)

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/4e1d6b79a2a743008f1ee6132be66b94.png)


### 2.4 烧录固件（均来自网络包括GitHub）
分享了两个固件，`Wi-PWN.9.0.english.bin`和`Wi-PWN.7.0.中文.bin`,我使用的是`Wi-PWN.7.0.中文.bin`

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/f9c2ceb6c3d3443e9a750ee38e2e524c.png)





---
# ESP8266---安装驱动
## 1.打开软件程序
>驱动程序已经分享放在材料准备中，直接双击打开文件

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/7fe26780f9fb40b8b7697bcf00ee2b61.png)

## 2.点击安装

>点击安装就可以

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/14985650f6f24684a08fecb72024c9a7.png)

## 3.安装完成
>安装成功

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/5360802563cf45caa82f65ef61807c89.png)


# ESP8266（烧录）
## 1.选择端口
>==**如果不自动显示COM端口，检查连接线，检查驱动安装，还不行就重启**==

>打开的烧录工具==ESP8266Flasher.exe==，选择自己的com端口：==我的是COM5==，点击倒三角是会显示你的端口的

>温馨提示：烧录工具（包括==32位==和==64位==）程序和烧录固件全部都==分享放在了（材料准备）里面==了，网盘分享的，注意查看

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/e476f804074e46b8ab75f74dff962448.png)

Operation：操作（设置烧录的端口）
Config：配置（设置烧录的文件）
Advanced：高级（设置烧录的速率）
About：关于
Log：日志
COM Port：COM 端口
Flash(F)：闪存
AP MAC：不知道是什么求大佬讲解
STA MAC：不知道是什么求大佬讲解

## 2.选择烧录文件
>在`Config`中配置`烧录的文件`
>在`Operation`中配置`烧录端口`
>`Advanced我没有配置`，如果烧录失败在配置吧，如果有烧录失败的朋友`留言或私信我学习一下`
>烧录失败配置`Advanced`中的`Baudrate`为`115200`

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/828f78d4e645495284b852728259a1f6.png)

## 3.灵魂汁子，烧给~
>确认`COM无误`后点击`Flash`按钮,就可以烧录了

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/bc569a089a2d43d5b903e805242cccdf.png)
## 4.烧录完成
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/2fd66e53afe44998b6a8cd395b7bbbec.png)


# ESP8266（擦除）
在 `Windows`中利用`python`中的`esptool`库中的命令对`ESP8266`的闪存程序进行`擦除 `

## 1.安装esptool库

```bash
pip3 install esptool
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/be82321e12c6408dabf7df79b507b858.png)

## 2.测试安装情况
注意是`esptool`不是`esptool.py`，没有==py==后缀
```bash
esptool
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/3f1d91f6df1d4110a88537f3fe06cf74.png)

## 3.查看ESP8266连接端口

>通过按 `Windows 键 + X 键 `并从菜单中选择“`设备管理器`”来打开设备管理器

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/b96398258fc149c6afcdc166540bf966.png)
>查找端口号的设备。它应该列在`端口（COM 和 LPT）`下，图中的端口为：COM5

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/cffb49589c8440ab92e2ed3060f5febc.png)
## 4.擦除命令

>使用`esptool`输入擦除命令，对ESP8266擦除
>👇
>请注意，如果您看到`“Connecting…”`消息后出现新的点，则表明您的 `ESP8266 未处于闪烁模式`。您将需要重复前面描述的所有步骤并再次按下`FLASH`按钮以确保您的ESP8266进入闪烁模式并成功完成擦除过程。

```bash
esptool --chip ESP8266 -p <USB端口> erase_flash
::其中<USB端口>为端口，不区分大小写，例如下
esptool --chip ESP8266 -p COM5 erase_flash
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/0a4ace7df2744f989cfa89a7dad64630.png)

# ESP8266（利用）
>==如果大家需要最新版请留言，多的很我在汉化最新版，下面这个是7.0，目前最新是9.0==
## 1.连接wifi
>烧录完成后，重新拔插一下ESP8266，会弄出一个开放式的网络：==Wi-PWN==，使用电脑连接WIFI

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/8f30eb0d19e8481f91ab58403b745e8e.png)
## 2.访问WI-PWN

>使用电脑访问==192.168.4.1==，点击继续

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/694eb6022ebc4d20a20ebd599287ec1d.png)

## 3.设置初始化名称和密码
>第一次使用会让你设置wifi名称和密码

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/0f0c13220da14cc89214f435d387c486.png)

## 4.重新连接
>设置完成后会自己重启，需要重新连接WIFI，重启连接后继续访问==192.168.4.1==，自动扫描附近的wifi，并选择需要攻击的wifi

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/44c963e2d1224d0f94581ef718f8a670.png)


## 5.攻击方式（功能介绍）
>攻击方式有很多种，下面四种均有讲解，看不懂请留言

 1. **Deauth**：无线网络拒绝服务攻击，模拟客户端断开连接时向路由器发送的断开帧，从而阻止客户端的连接传输，（对5GHz频段无效）
 2. **Beacon**：通过不断发送信标帧数据包来干扰对方的正常连接，迷惑用户。这种攻击可以自定义SSID或者随机生成48个热点来迷惑对方
 3. **Random 5秒**：每五秒随机保存48个SSID，配合`Beacon`使用
 4. **Probe-Request**：请求认证攻击，让客户端误认为范围内存在曾经连接过的WiFi热点（但是我没试出来）
 
![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/6db04fe0d5f349a7a7c9376e468b05be.png)

## 6. 效果图展示
>`Beacon`功能的效果图展示

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/44b3567d286447589d9d5bc832556f69.jpeg)




---
# esptool（各种报错解决）
## 报错1（端口输入错误）
>大概率是因为端口写错了，检查端口，换了USB口插入会改变端口，如果不是请留言我也看看

```bash
C:\Users\17569\Desktop>esptool -p COM0 erase_flash
esptool.py v4.7.0
Serial port COM0

A fatal error occurred: Could not open COM0, the port is busy or doesn't exist.
(could not open port 'COM0': FileNotFoundError(2, '系统找不到指定的文件。', None, 2))

Hint: Check if the port is correct and ESP connected


C:\Users\17569\Desktop>
```
---

## 报错2（擦写报错）
>在设备管理器中找到设备后卸载设备，然后拔插一下就好了
```bash
C:\Users\17569>esptool --chip ESP8266 -p COM1 erase_flash
esptool.py v4.7.0
Serial port COM1

A serial exception error occurred: Cannot configure port, something went wrong. Original message: PermissionError(13, '连到系统上的设备没有发挥作用。', None, 31)
Note: This error originates from pySerial. It is likely not a problem with esptool, but with the hardware connection or drivers.
For troubleshooting steps visit: https://docs.espressif.com/projects/esptool/en/latest/troubleshooting.html


上面报错，卸载设备后拔插恢复了


C:\Users\17569>esptool --chip ESP8266 -p COM3 erase_flash
esptool.py v4.7.0
Serial port COM3
Connecting....
Chip is ESP8266EX
Features: WiFi
Crystal is 26MHz
MAC: 8c:aa:b5:0d:95:5c
Uploading stub...
Running stub...
Stub running...
Erasing flash (this may take a while)...
Chip erase completed successfully in 8.5s
Hard resetting via RTS pin...

C:\Users\17569>
```




# 参考文章

[ESP8266 NodeMCU 擦除闪存执行出厂重置_esp8266恢复出厂设置-CSDN博客](https://blog.csdn.net/ICMRCHIP/article/details/131305586)
[ESP-8266固件擦除以及烧录_esp8266擦除固件-CSDN博客](https://blog.csdn.net/hush777/article/details/127642899)
[擦除 ESP8266 开发板 FLASH 闪存的方法– 树莓派 Pico 实验室（RP2040）](https://pico.nxez.com/2019/03/23/pyboard-d-series-development-board-released.html)
[Wi-PWN（现代 ESP8266 Deauther）| Hackaday.io](https://hackaday.io/project/23305-wi-pwn-modern-esp8266-deauther)
[GitHub samdenty/Wi-PWN: ESP8266 firmware for performing deauthentication attacks, with ease.](https://github.com/samdenty/Wi-PWN)
[GitHub SpacehuhnTech/esp8266_deauther: Affordable WiFi hacking platform for testing and learning](https://github.com/SpacehuhnTech/esp8266_deauther)
[ESP8266开发板刷WI-PWN固件（wifi杀手）教程（详细）_wi-pwn ch-CSDN博客](https://blog.csdn.net/qq_42294237/article/details/119905076)
[记录一次ESP8266开发板刷WI-PWN固件（WiFi杀手）操作（含固件烧制工具等）_esp8266flasher.exe-CSDN博客](https://blog.csdn.net/Wiofgb/article/details/126323167)
[wifi中断攻击_Flasher_deauth_wi-pwn](https://www.sohu.com/a/505171965_120743310)
[wifi杀手-漏洞产生原因和防御措施 - 知乎](https://zhuanlan.zhihu.com/p/598456333)
[Release Version 8.0 · samdenty/Wi-PWN](https://github.com/samdenty/Wi-PWN/releases/tag/8.0)
[micropython esp8266刷固件_esp8266flasher下载-CSDN博客](https://blog.csdn.net/weixin_40570700/article/details/118079007)
[ESP8266使用入门教程 - crazyyang - 博客园](https://www.cnblogs.com/sgy2782308186/articles/9594992.html)
[利用ESP8266模块制作便携WiFi杀手进行deauth攻击-腾讯云开发者社区-腾讯云](https://cloud.tencent.com/developer/article/1933693?areaId=106001)
[ESP8266开发板之WIFI_Killer烧录-腾讯云开发者社区-腾讯云](https://cloud.tencent.com/developer/article/1957653)
[ESP8266-nodeMCU-I2c-12864-写个三行情书_esp8266flasher.exe-CSDN博客](https://blog.csdn.net/chenqide163/article/details/84801274)
[ESP8266Wifi模块制作Wifi杀手【4】-小叶白龙博客](http://www.xiaoyebailong.com/index.php/2020/05/04/68555.htm)
[手把手教你制作基于esp8266的WIFI杀手 - 程序员大本营](https://www.pianshen.com/article/20372360746/)
[ESP8266 | 简单的WIFI杀手和克隆 来自 brave](http://www.360doc.com/content/22/1203/18/37237925_1058688606.shtml)
[Wi-Fi杀手（Wi-Fi kill）的原理是什么？如何从技术上阻止这种侵害？ - 知乎](https://www.zhihu.com/question/27015381)
[记录一次ESP8266开发板刷WI-PWN固件（WiFi杀手）操作（含固件烧制工具等） - overfit.cn](https://avoid.overfit.cn/post/b6a4821c490648ea8528b83373f9b2ed)
[低成本ESP8266制作WIFI杀手-给楼下嗨翻天的老哥戒网瘾 - 哔哩哔哩](https://www.bilibili.com/read/cv5291433/)
[wifi杀手，教你不拔网线也能断网](http://www.360doc.com/content/23/1219/17/83910170_1108112651.shtml)
[利用ESP8266制作wifi杀手并进行攻击-漏洞产生原因及防御措施-腾讯云开发者社区-腾讯云](https://cloud.tencent.com/developer/article/2359321)
[ESP8266-WIFIkiller讲解-CSDN博客](https://blog.csdn.net/gcweb666/article/details/129187909)
[低成本ESP8266制作WIFI杀手-给楼下嗨翻天的老哥戒网瘾 - 哔哩哔哩](https://www.bilibili.com/read/cv5291433/)
[【图片】39元,ESP-8266模块做一个便携式wifi杀手渗透局域网，钓鱼测试_渗透吧_百度贴吧](https://tieba.baidu.com/p/6293810625)
[Wi-Fi杀手（Wi-Fi kill）的原理是什么？如何从技术上阻止这种侵害？ - 知乎](https://www.zhihu.com/question/27015381)
[常见的WiFi攻击技术及检测方法总结](https://www.sohu.com/a/194831500_99907709)
[ProbeQuest：一款功能强大的Wi-Fi探测请求捕捉和嗅探工具 - FreeBuf网络安全行业门户](https://www.freebuf.com/sectool/380043.html)
[利用ESP8266制作wifi杀手并进行攻击-漏洞产生原因及防御措施-腾讯云开发者社区-腾讯云](https://cloud.tencent.com/developer/article/2359321)
[此错误源自 pySerial。这可能不是 esptool 的问题，而是硬件连接或驱动程序的问题 - ESP32 Forum](https://esp32.com/viewtopic.php?p=127356)
[ESP8266 NodeMCU 擦除闪存执行出厂重置_esp8266恢复出厂设置-CSDN博客](https://blog.csdn.net/ICMRCHIP/article/details/131305586)
[ESP8266刷出厂固件 esp8266怎么恢复出厂设置_桃太郎的技术博客_51CTO博客](https://blog.51cto.com/u_12204/10179814)
[ESP8266恢复出厂设置-CSDN博客](https://blog.csdn.net/wxs_hello/article/details/115647316)
[工具｜乐鑫科技](https://www.espressif.com.cn/zh-hans/support/download/other-tools)
[ESP32固件烧录方法（三种方法实现）_esp32烧录-CSDN博客](https://blog.csdn.net/weixin_45477686/article/details/135020526)
[在macOS 上使用 esptool 烧录合宙ESP32C3 开发板 micropython 固件遇到的问题与解决办法_esptool烧录固件-CSDN博客](https://blog.csdn.net/weixin_43821212/article/details/131648656)
[esp8266开源烧录工具--esptool_那段杂年华_新浪博客](https://blog.sina.com.cn/s/blog_ed2c83c30102xcdv.html)
[烧写固件 | DoitCar 开发流程](http://nodemcu-dev.doit.am/2.html)
