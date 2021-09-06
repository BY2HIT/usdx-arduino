**uSDX – 基于Arduino的短波SDR收发信机**
-

最初由PE1NNZ在QRP Labs销售的CW收发信机套件[QCX](https://github.com/threeme3/QCX-SSB/)（非开源）的基础上魔改，小幅度更改了硬件，并编写了开源版本软件，实现了SSB等多种模式的收发。随后，多名爱好者分别开发了开源版本的硬件。主要优点是体积小、结构简单、成本低、全模式。

一篇英文介绍文章：[https://qrper.com/2020/09/an-introduction-to-the-usdx/](https://qrper.com/2020/09/an-introduction-to-the-usdx/)

**主要特性：**
- ATMega328实现界面+信号处理，Arduino软件框架；
- 1602/0.91 inch OLED显示，编码开关、按钮开关输入;
- 支持CW/SSB/AM等，发射功率3~5 W;
- 接收机采用零中频/低中频架构，ATMega328内置ADC双路采样；
- 发射机通过PWM控制功率放大器的电源电压实现幅度调制，通过高速I2C（800 kbps）控制时钟发生器SI5351的瞬时输出频率实现相位调制。

**改进目标：**
- 进行模块化设计，Arduino UNO盾板形式，MCU+IO时可作为开发板，MCU+IO+RF时作为电台；
- 增加磁棒天线、拉杆天线、单向按钮，实现80米测向机功能。
- 增加CW自动发送、天线调谐器，实现80米测向信号源功能。

**uSDX软件**

[https://github.com/threeme3/QCX-SSB/](https://github.com/threeme3/QCX-SSB/)

**uSDX硬件**

WB2CBA和Antrak设计的单PCB、可换低通滤波器版：[https://antrak.org.tr/blog/projeler/usdx-an-arduino-based-sdr-all-mode-hf-transceiver-pcb-iteration-v1-02/](https://antrak.org.tr/blog/projeler/usdx-an-arduino-based-sdr-all-mode-hf-transceiver-pcb-iteration-v1-02/)

DL2MAN设计的层叠PCB多波段版：[https://dl2man.de/](https://dl2man.de/)

BG6JJI设计的多波段版（嘉立创工程）：[https://oshwhub.com/jerrych/usdx_copy_copy_copy_copy_copy_copy_copy_copy_copy](https://oshwhub.com/jerrych/usdx_copy_copy_copy_copy_copy_copy_copy_copy_copy)

**0.2.0版样机**
已知bug已全部修正！
![usdx0813a](https://user-images.githubusercontent.com/2872962/132234040-b0993e06-f292-4fc8-9b33-6c5535261b1a.jpg)
![usdx0813b](https://user-images.githubusercontent.com/2872962/132234048-43afcc40-3e3a-4a54-b5fe-b3f2a148c6b2.jpg)
