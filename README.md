# 移植 emWin 与 HAL 库结合

目前正点原子只给出 emWin 与标准库的组合，移植 emWin 与 HAL 库结合。因移植比较困难，小坑比较多（采用正点原子风格的项目结构，非通用结构，如 cubeMX 生成），故建立此项目。

此项目结构较为古老，且 emWin 闭源且需付费，建议使用其他现代的开源GUI库。

## F1_HAL_emwin

### 移植组合

正点原子式 STM32 项目结构 + 正点原子库 + HAL 库 + STemWin

### 实现

默认实现为 emWin 官方 Demo

试验成功支持：STM32F103ZET6

> 更多实现参考： [framist/E-kit: E-kit 一体化电子工具箱，STM32 实现，示波器+函数发生器+... (github.com)](https://github.com/framist/E-kit) 增加多页支持结构，支持GUIBuilder

### 性能测试

Demo8：像素填充测试，最好成绩。

| 环境                                      | Pixels/sec |
| ----------------------------------------- | ---------- |
| STM32F103ZET6,-O2                         |            |
| STM32F103ZET6,-O3                         |            |
| STM32F103ZET6,-O2（正点原子，结合标准库） | `6123000`  |


## F4_HAL_emwin
### 移植组合

正点原子式STM32项目结构 + 正点原子库 + HAL 库 + STemWin

采用外部SRAM，FPU，DSP_LAB

### 实现

默认实现为 emWin 官方 Demo

试验成功支持：STM32F407ZGT6

### 性能测试

Demo8：像素填充测试，最好成绩。

| 环境                    | Pixels/sec |
| --------------------------- | ---------- |
| STM32F407ZGT6,-O2                         | `21600000` |
| STM32F407ZGT6,-O3                         | `20900000` |
| STM32F407ZGT6,-O2（正点原子，结合标准库） | `21105000` |



---

<img src="README/LETA.jpg" alt="LETA" style="zoom: 24%;" />
