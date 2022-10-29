# ESP32-VFD-8DM-Drive
*Futaba VFD display (8-MD-06INKM) driver for Arduino（本项目使用platformio平台开发）*

## 1. 说明

- 类名称为VFD_Display
- VFD.h为驱动头文件
- VFD.cpp为驱动主程序
- main.cpp为提供的示例程序

## 2. 函数

| 序号 | 函数名                                                       | 参数                                               | 用途                                            |
| ---- | ------------------------------------------------------------ | -------------------------------------------------- | ----------------------------------------------- |
| 1    | *void* VFD_Init()                                            | **NONE**                                           | 初始化VFD屏幕,包括初始化SPI                     |
| 2    | *void* VFD_Clear(*char* **bit**)                             | **bit**:显示位                                     | 清空指定位的显示,当bit未指定时,清空所有位的显示 |
| 3    | *void* VFD_Show(*char* **bit**, String / char **str / char**) | **bit**:显示位   **str / char**:要显示的字符（串） | 在指定位之后显示字符(串)                        |
| 4    | *void* VFD_Set_cmd(byte **cmd**, byte **data**)              | **cmd**:命令  **data**:数据                        | 直接向VFD发送指令                               |
| 5    | *void* VFD_Show_custdata(*char* **bit**, *char* **flag**)    | **bit**:显示位  **flag**:图像的标志                | 显示自定义的图像                                |
| 6    | *void* VFD_Standby_mode(*bool* **mode**)                     | **mode**:待命模式开启                              | VFD省电模式开启与关闭                           |
| 7    | *void* VFD_Display_status(*bool* **status**)                 | **status**:显示屏开启关闭                          | VFD显示开启与关闭                               |
| 8    | *void* VFD_Set_dimming(byte **dimming**)                     | **dimming**:显示亮度                               | 设置VFD的显示亮度(范围0 ~ 255)                  |
| 9    | *void* VFD_Write_custdata(*char* **flag**, *const* byte * **data**) | **flag**:要写入到的标志 ***data**:图像的数组       | 向VFD写入自定义图像                             |
| 10   | *void* VFD_FadeIn(byte **pertime**)                          | **pertime**:每次延迟的时间                         | VFD的淡入的效果                                 |
| 11   | *void* VFD_FadeOut(byte **pertime**)                         | **pertime**:每次延迟的时间                         | VFD的淡出的效果                                 |
| 12   | *void* VFD_RDnum(*char* **bit**)                             | **bit**:要乱码的位                                 | VFD的单个位乱码效果                             |

