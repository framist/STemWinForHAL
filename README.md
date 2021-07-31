# 移植emWin与HAL库结合

目前正点原子只给出emWin与标准库的组合，移植emWin与HAL库结合。因移植比较困难，小坑比较多（采用正点原子项目结构，非通用结构，如cubeMX生成），故建立此项目。

## F1_HAL_emwin

移植组合：

正点原子式STM32项目结构 + 正点原子库 + HAL库 + STemWin

默认实现~~为emWin官方Demo~~ [framist/E-kit: E-kit 一体化电子工具箱，STM32实现，示波器+函数发生器+... (github.com)](https://github.com/framist/E-kit) 增加多页支持结构，支持GUIBuilder

试验成功支持：STM32F103ZET6

## F4_HAL_emwin
移植组合：
正点原子式STM32项目结构 + 正点原子库 + HAL库 + STemWin

采用外部SRAM，FPU，DSP_LAB

默认实现为emWin官方Demo

试验成功支持：STM32F407ZGT6

