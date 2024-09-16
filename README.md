# ESP32-VFD-8DM-Drive

English | [简体中文](README_CN.md)

*Futaba VFD display (8-MD-06INKM) driver for Arduino (This project is developed using the platformio platform)*

## 1. Description

- Class name: VFD_Display
- VFD.h: Header file for the driver
- VFD.cpp: Main program for the driver
- main.cpp: Example program provided

## 2. Functions

| No.  | Function Name                                                | Parameters                                                   | Purpose                                                      |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1    | *void* init()                                                | **NONE**                                                     | Initialize the VFD screen, including SPI initialization      |
| 2    | *void* clear(*char* **bit**)                                 | **bit**: Display bit                                         | Clear the display of the specified bit, when bit is not specified, clear the display of all bits |
| 3    | *void* show(*char* **bit**, String / char **str / char**)    | **bit**: Display bit   **str / char**: Character (string) to display | Display the character (string) after the specified bit       |
| 4    | *void* setCmd(byte **cmd**, byte **data**)                   | **cmd**: Command   **data**: Data                            | Send a command directly to the VFD                           |
| 5    | *void* showCustdata(*char* **bit**, *char* **flag**)         | **bit**: Display bit   **flag**: Flag for the image          | Display a custom image                                       |
| 6    | *void* standbyMode(*bool* **mode**)                          | **mode**: Standby mode enable                                | Enable or disable VFD power-saving mode                      |
| 7    | *void* displayStatus(*bool* **status**)                      | **status**: Display on/off                                   | Turn the VFD display on or off                               |
| 8    | *void* setDimming(byte **dimming**)                          | **dimming**: Display brightness                              | Set the display brightness of the VFD (range 0 to 255)       |
| 9    | *void* writeCustdata(*char* **flag**, *const* byte * **data**) | **flag**: Flag to write to   ***data**: Image array          | Write custom image to VFD                                    |
| 10   | *void* fadeIn(byte **pertime**)                              | **pertime**: Delay time per step                             | Fade-in effect for VFD                                       |
| 11   | *void* fadeOut(byte **pertime**)                             | **pertime**: Delay time per step                             | Fade-out effect for VFD                                      |
| 12   | *void* RDnum(*char* **bit**)                                 | **bit**: Bit to display gibberish                            | Display gibberish for a specific bit on VFD                  |
