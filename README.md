2018-12-26

一.第一版

2019-1-24

一.修改触摸的驱动使其有自动校正的功能！






2019-3-22

一.更新SDK中各个工程的协议栈lib文档，涉及的文件如下：

"SYD8811_SDK\Source Code\SYD8811_ble_peripheral\3.SYD8811_HID\ble\syd8811_ble_lib.lib"

"SYD8811_SDK\Source Code\ble\syd8811_ble_lib.lib"

"SYD8811_SDK\Source Code\SYD8811_ble_peripheral\1.SYD8811_UART original\ble\syd8811_ble_lib.lib"

"SYD8811_SDK\Source Code\SYD8811_ble_peripheral\1.SYD8811_UART\ble\syd8811_ble_lib.lib"

"SYD8811_SDK\Source Code\SYD8811_ble_peripheral\2.SYD8811_UART_Capdet_Touch\ble\syd8811_ble_lib.lib"



2019-5-22
一、整理Source Code工程的架构，各个文件功能说明如下

<1> Driver、Include、Rtt存放8811相关的外设驱动文件

<2> BLE文件夹存放OTA升级相关文件

<3> Lib文件夹存放协议栈lib、软件定时器lib、触摸lib

<4> SYD8811_ble_peripheral文件夹存放8811 BLE相关例程（透传、HID）

<5> SYD8811_peripheral文件夹存放8811外设相关例程（ADC、PWM、IIC、TIMER、RTC等）

二、更新协议栈lib    "SYD8811_SDK\Source Code\Lib\syd8811_ble_lib.lib"
三、按照规定格式，整理SYD8811_ble_peripheral文件夹和SYD8811_peripheral文件夹的各个工程
四、更新Documentation文件下8811手册

<1>、《SYD8811_BLE_DS_v1p1_CN_20190508》

<2>、《SYD8811_BLE_DS_v1p2_EN_20190508》

五、更新tool文件夹下SYDTEK Studio tool

<1>、《SYDTEK Studio release20190521》

六、更新《SYD8811_SDK\Source Code\SYD8811_peripheral》目录下各工程头文件引索目录，比如ADC工程中把“..\adc”改成“..\”
七、修改《SYD8811_SDK\Source Code\SYD8811_peripheral》目录下各工程的《config.h》文件，增加“#define _DEBUG_”一句话，使用宏“_DEBUG_”让工程往UART输出log
八、删除《SYD8811_SDK\Source Code\Include\syd_type.h》文件以及各个工程对其的引用
九、增加文件："SYD8811_SDK\Documentation\SYD8811_pinmux_table_20190527.xlsx"，对SYD8811的pinmux进行介绍





2019-6-10 

修改《SYDTEK Studio  release20190610v3.5.0 》

一、这里务必使用最新的tool，原来的tool可能会出现意想不到的情况！

二、增加文章"SYD8811_SDK release\Documentation\SYD8811内存和代码的分布.pdf"

三、修改了所有带BLE的工程的“profile”文件夹，在OTA的服务中增加上“write without Rspone"属性

四、增加工程《SPI_Master_FLASH_limiting_speed》

五、增加工程《uart1_debug》

六、增加工程《4.SYD8811_BLE_UART_GPIO_open_power》

七、增加工程《5.SYD8811_BLE_UART_EVBOLED_Scan》

八、修改Hpwm的驱动，主要体现在：HPWM_IRQHandler和Hpwm_Init函数！     






2019-7-5

一、增加工程《SYD8811_SDK\Source Code\SYD8811_peripheral_misc\SYD8811_BLE_UART_EVBOLED_notifyen_open_power_XTAL》

二、修改RTT的驱动，使其能够输出浮点函数，替换       

三、使用最新版本的《SYDTEK Studio》，版本号为《V3.8.9 20190628.7z》

四、增加工程《SYD8811_SDK\Source Code\SYD8811_peripheral_misc\CLK_XO16_To_Gpio》






2019-7-15

一、增加工程《"SYD8811_SDK\Source Code\SYD8811_peripheral_misc\flash_internal_custom_3k"》

二、增加工程《"SYD8811_SDK\Source Code\SYD8811_peripheral_misc\flash_internal_custom_Anysize"》

三、把涉及到BLE的项目使用timer0改为使用timer1，因为软件定时器系统也使用timer0，涉及到的项目有：

A.SYD8811_SDK\Source Code\SYD8811_ble_peripheral\1.SYD8811_BLE_UART_notifyen_open_power

B.SYD8811_SDK\Source Code\SYD8811_ble_peripheral\3.SYD8811_BLE_UART_EVBOLED_notifyen_open_power

C.SYD8811_SDK\Source Code\SYD8811_ble_peripheral\4.SYD8811_BLE_UART_GPIO_open_power

E.SYD8811_SDK\Source Code\SYD8811_ble_peripheral\5.SYD8811_BLE_UART_EVBOLED_Scan

F.SYD8811_SDK\Source Code\SYD8811_peripheral_misc\SYD8811_BLE_UART_EVBOLED_MAC

G.SYD8811_SDK\Source Code\SYD8811_peripheral_misc\SYD8811_BLE_UART_EVBOLED_notifyen_open_power_verdor_datas

H.SYD8811_SDK\Source Code\SYD8811_peripheral_misc\SYD8811_BLE_UART_EVBOLED_notifyen_open_power_XTAL

I.SYD8811_SDK\Source Code\SYD8811_peripheral_misc\SYD8811_BLE_UART_LowPower

J.SYD8811_SDK\Source Code\SYD8811_peripheral_misc\SYD8811_BLE_UART_notifyen_open_power_restartadv

修改在send_to_master和timer_1_callback两个函数中
