# My Raspberry Pi Setup

- Raspberry Pi 4 Model B 8GB RAM
- Металлический корпус-радиатор для raspberry pi 4
- Карта памяти Kingston Canvas Select Plus microSDXC 64 ГБ [SDCS2/64GBSP] (
- Мобильная клавиатура Vontar V2818 беспроводная 033
- Power Bank Xiaomi 20000 mAh USB-C (5В 3А)

_Карту памяти нужно брать Class 10_

## Параметры монитора

### User Manual JRP7006/JRP1105

У меня модель JRP7006
Подключение монитора идет через HDMI и через USB-C --- 2x USB-A

☐ - display 
🍓 - малина

☐  USB C ---< USB A + USB A  🍓 
☐  miniHDMI --- HDMI + Adapter micro HDMI  🍓 

【Product Descriotion】
- 7 inch standard display, 1024 × 600 Hardware resolution, Up to 1920x1080 Software configuration resolution.
- Capacitive touch screen, maximum support 5 point touch.
- Support backlight control alone, the backlight can be turned off to save power.
- Support Raspberry Pi, BB Black, Banana Pi and other mainstream mini PC.
- Can be used as general-purpose-use HDMI monitor, for example: connect with a computer HDMI as the sub-display.
- Used as a raspberry pi display that supports Raspbian, Ubuntu, Kali-Linux, Kodi, win10 IOT, single-touch, free drive.
- Work as a PC monitor, support win7, win8, win10 system 5 point touch (XP and older version system: single-point touch), free drive.
- CE, RoHS certification.

【Product Parameters】
_Resolution: 1024 x 600 (dots)_
_Touch: five-point capactive touch_

【Hardware Description】

![JRP7006](https://github.com/frenkel2901/MyRaspberrySetup/blob/main/display.jpg?raw=true)

【How to use with Raspbian/Ubuntu Mate/Win10 IoT Core System

- Step 1, Install Raspbian official image (Или любой другой образ, например Kali)

1) Download the latest image from the official download.
2) Install the system according to the official tutorial steps.

- Step 2, modify the “config.txt”

After the programming of Step1 is completed, open the config.txt file of TF card root directory and add the following code at the end of the file, save and eject Micro SD Card safely:

```
~~max_usb_current=1~~ Эту строку я не использую

hdmi_force_hotplug=1
config_hdmi_boost=7
hdmi_group=2
hdmi_mode=87
hdmi_drive=1
display_rotate=0
hdmi_cvt 1024 600 60 6 0 0 0
```

- Step 3, Drive the 7inch HDMI JRP7007 with the Raspberry Pi

Insert the TF Card to Raspberry Pi, connect the Raspberry Pi and LCD by HDMI cable;
connect USB cable to one of the four USB ports of Raspberry Pi,and connect the other end of the USB cable to the USB port of the LCD;
then supply power to Raspberry Pi; after that if the display and touch both are OK,it means drive successfully (please use the full 3A for power supply).

