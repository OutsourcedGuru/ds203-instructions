# ds203-instructions
Instructions for using the SainSmart Mini DSO DS203 pocket-sized oscilloscope (the unauthorized manual)

![ds203](https://cloud.githubusercontent.com/assets/15971213/25502069/f7bf9d02-2b49-11e7-9c96-87c461e45e51.png)

## Features
* Battery-powered, portable, pocket-sized
* Lightweight (2 ounces)
* Full-Color 3" LCD 400x240 display
* 4 channels (two digital - CH C/D, two analog - CH A/B)
* 8MHz Analog Bandwidth
* 72MSps sample rate, 8-bit
* User-upgradeable firmware via USB tethering to include some customization
* Digital storage of data with HOLD for analysis (with memory depth of 4K/channel, 2MB internal USB disk, optionally 8MB) with playback
* Four programmable spaces for user applications, open-source
* 2 Mueller mcx oscilloscope probes included (X1, X10)
* Vertical scale: 20mV-10V/division (using X1 probe)
* Horizontal sensitivity: 0.1µS/division - approximately 1S/division
* Horizontal position: adjustable
* Input coupling: AC/DC
* Input impedance: > 800kΩ
* Max input voltage: 80Vpp (with X1 probe)
* Software trigger type: edge, pulse (auto, normal, single, scan, none)
* Hardware trigger type: edge
* Trigger soure: CH1/CH2/EXT
* Signal generator: 10Hz to 1Mhz (square, sin, sawtooth, triangle) **Reported as 10-20K Hz in ElecHouse's manual**
* Auto measure: Vmax, Vmin, Vpp, Vavr, Vrms, Freq, Period, Pulse, Duty cycle, Vdc, Vbt, FPS
* Current measurement: Level, Voltage
* Display modes: CH1, CH2, EXT, CH1 + CH2, CH1 - CH2, CH1 * CH2
* Sampling mode: realtime
* Sampling rate: 1k - 72M samples/second
* Power: Li-ion battery
* Dimensions: 98mm * 60mm * 14.5mm
* Weight without battery: 80g (shipping weight 1.2lbs)
* Processor: ARM cortex M3 (STM32VCT6) 32-bits with integrated FPGA and high-speed ADC
* ASIN: B0057M7YLE

## Existing Documentation
[From Sainsmart.com's website (PDF, 13 pages)](http://www.sainsmart.com/zen/documents/20-010-201/DSO203Manual.pdf)
[From ElecHouse.com's website (PDF, 29 pages)](http://www.elechouse.com/elechouse/images/product/DS203/DS203_Manual.pdf)

## Interface and Controls
The following controls are broken down by side of the oscilloscope, as held vertically to face the LCD screen. **Note that ElecHouse's button listing on their p5 incorrectly labels CH-A and CH-B locations**

### Top
* K1: Also known as PLAY or Run/Hold
* K2: Also known as STOP or Calibrate
* K3: Also known as RECORD or Preset
* K4: Also known as TRIANGLE or Save Wave
* NAV A: Also known as "-..v..+" or Navigator A
* NAV B: Also known as "<..v..>" or Navigator B

### Left
* WAVE OUT: Signal generator output, mcx-style connector
* CH B: Analog channel 2, mcx-style connector
* CH A: Analog channel 1, mcx-style connector

### Right
* CH C: Digital channel 3, mxc-style connector
* CH D: Digital channel 4, mxc-style connector
* USB port: Mini-USB style (rather than the slightly more popular micro-USB style) connector
* Power switch: standard, sliding switch

### LCD-based
The following is a list of menus seen on the LCD screen during operation after the initial splashscreen.

#### Top-most menu
Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently. For the top two menus, what is seen in adjacent cells are connected to each other. In other words, "1V" in my case in the second menu row refers to the setting for "AC" which corresponds to the setup for analog CH A. The same is true for "AC" + "1V" for CH B. The same is true for digital CH C which I am currently not displaying ("--"), for example. The last three menu items on the top menu correspond to the last menu item graphic on the second top menu since they go together.
* RUN
* AC
* AC
* CH(C)
* CH(D)
* AUTO
* Squ with a small graphic of two cycles of a square wave
* 10KHz
* DUT 50%

#### Second from top menu
Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently.
* Battery charge indicator
* 1V
* 1V
* --
* --
* 20µS
* Small graphic of current selection of stored waveform

#### Right-side menu
Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently.
* Unknown
* THR
* V1
* V2
* T1
* T2
* Y
* X
* T0
* 4K
* EXT

#### Bottom display-only data
The values seen here are not menu items and may not be selected. These are usually the result of setting up on-screen V1/V2/T1/T2 references to measure signals. Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently.
* ΔV: +4.80V
* ΔT: +133 µS
* Vbt +4.15V 
