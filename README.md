
# Board Support Package (esp-bsp component) using ESP-IDF 5.3, ili9341 LCD and LVGL 9.x modified for esp32-cam

Esp32-cam connected to 2.8" ili9341 LCD display using LVGL for video stream.
This project requires the esp-idf sdk 5.3.1.

 ## Display Pins
 
| Pin Number on ILI9341 Display  | Pin Number on ESP32-cam |
| ----------- | ----------- |
| 3.3V     | 3.3V       |
| GND      | GND   |
| CS| 12  |
| RST | 2   |
| DC | 13  |
| MOSI | 15 |
| CLK | 14  |
| LED | 3.3V |
| MISO | NC  |

## LVGL configuration settings

#### You can choose to build with the default LVGL configuration settings from:

`idf.py menuconfig`

`Menu → Component config → LVGL configuration → Memory Settings:`

#### and:

```
Malloc functions source (Standard C functions malloc/realloc/free) --->  

String functions source (Standard C functions memcpy/memset/strlen/strcpy) --->   

Sprintf functions source (Standard C functions vsnprintf) --->
```

#### or change to custom

` LVGL's built in implementation ` settings *(included in ` sdkconfig.defaults ` )*:

```
(64) Size of the memory used by lv_malloc() in kilobytes (>= 2kB)

(0) Size of the memory expand for lv_malloc() in kilobytes

(0x0) Address for the memory pool instead of allocating it as a normal array
```

https://github.com/user-attachments/assets/57fe843d-6d39-4114-9fc7-1b7ccc4c6532



![terminal](https://github.com/user-attachments/assets/7b17a434-453d-41e2-ad47-601f8f8c8a1a)


