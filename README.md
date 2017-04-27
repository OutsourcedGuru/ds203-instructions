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
* Signal generator: 10Hz to 1Mhz (square, sin, sawtooth, triangle) *Reported as 10-20K Hz in ElecHouse's manual.*
* Auto measure: Vmax (maximum voltage), Vmin (minimum voltage), Vpp (Peak-to-peak voltage), Vavr, Vrms (Average value of voltage), Freq (signal frequency), Period, Pulse, Duty cycle, Vdc (direct current voltage), Vbt, FPS (frames Per Second)
* Current measurement: Level, Voltage
* Display modes: CH1, CH2, EXT, CH1 + CH2, CH1 - CH2, CH1 * CH2
* Sampling mode: realtime
* Sampling rate: 1k - 72M samples/second
* Power: Li-ion battery
* Dimensions: 98mm * 60mm * 14.5mm
* Weight without battery: 80g (shipping weight 1.2lbs)
* Processor: ARM cortex M3 (STM32VCT6) 32-bits with integrated FPGA and high-speed ADC
* Temperature requirements: Operating (0°-50°C), Non-operating (-20° - +60°C)
* Humidity requirements: Operating (10-60% RH), Non-operating (5-60 % RH)
* Max transient-withstanding voltage: +/- 400V peak value
* Max input voltage of logic probe: +/- 15V peak value
* ASIN: B0057M7YLE

## MCX-style probe connection
![mcx](https://cloud.githubusercontent.com/assets/15971213/25506780/2fb8ba96-2b5d-11e7-94d8-7c496a05bf33.jpg)

## Existing Documentation
[From Sainsmart.com's website (PDF, 13 pages)](http://www.sainsmart.com/zen/documents/20-010-201/DSO203Manual.pdf)<br/>
[From ElecHouse.com's website (PDF, 29 pages)](http://www.elechouse.com/elechouse/images/product/DS203/DS203_Manual.pdf)

## Interface and Controls
The following controls are broken down by side of the oscilloscope, as held vertically to face the LCD screen. There appear to be short-press and long-press versions of the K1-K4 controls which perform different functions. *Note that ElecHouse's button listing on their p5 incorrectly labels CH-A and CH-B locations.*

### Top Controls
* K1: Also known as PLAY or Run/Hold (this is a momentary-press toggle button)
* K2: Also known as STOP or Calibrate (this is a momentary-press toggle button)
* K3: Also known as RECORD or Preset (this is a momentary-press toggle button, toggling this often brings up a popup display which is sometimes signal details)
* K4: Also known as TRIANGLE or Save Wave (this is a momentary-press toggle button)
* NAV-A: Also known as "-..v..+" or Navigator A (this momentary-press switch can be pushed left or right and the momentary-press middle can be pressed down as a toggle)
* NAV-B: Also known as "<..v..>" or Navigator B (this momentary-press switch can be pushed left or right and the middle can be pressed down)

### Left Inputs and Ouput
* WAVE OUT: Signal generator output, mcx-style connector
* CH-B: Analog channel 2, mcx-style connector
* CH-A: Analog channel 1, mcx-style connector

### Right Inputs, USB and Control
* CH-C: Digital channel 3, mxc-style connector
* CH-D: Digital channel 4, mxc-style connector
* USB port: Mini-USB style (rather than the slightly more popular micro-USB style) connector
* Power switch: standard, sliding switch

### LCD-based
The following is a list of menus seen on the LCD screen during operation after the initial splashscreen.

#### Top-most menu
Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently. For the top two menus, what is seen in adjacent cells are connected to each other. In other words, "1V" in my case in the second menu row refers to the setting for "AC" which corresponds to the setup for analog CH-A. The same is true for "AC" + "1V" for CH-B. The same is true for digital CH-C which I am currently not displaying ("--"), for example. The last three menu items on the top menu correspond to the last menu item graphic on the second top menu since they go together.
* RUN  (This appears to be a status indicator when toggling between displaying an active/changing waveform and displaying a frozen/held waveform for the purpose of measurements.)
* AC (This and the adjacent/lower cell control the analog CH-A input, when toggled indicates DC; however, pressing down toggles to HIDE) <span style="color:cyan">The color associated with CH-A is cyan.</span>
* AC (This and the adjacent/lower cell control the analog CH-B input, when toggled indicates DC; however, pressing down toggles to HIDE)  <span style="color:yellow">The color associated with CH-B is yellow.</span>
* CH(C) (This and the adjacent/lower cell control the digital CH-C input) <span style="color:purple">The color associated with CH-C is purple.</span>
* CH(D) (This and the adjacent/lower cell control the digital CH-D input but additionally shows modes A + B, A - B, C AND D, C OR D, REC A, REC B, REC C, REC D and hide CH-D) <span style="color:green">The color associated with CH-D is green.</span>
* AUTO (This appears to be the synchronous mode indicator and the adjacent/lower cell indicates the associated value.) <span style="color:brown">The color associated with synchronous mode is brown.</span>
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

#### Right-side menu ("Menu Group 2")
Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently.
* Unknown symbol
* THR <span style="color:cyan">The color associated with CH-A is cyan if it is currently selected.</span>
* V1 <span style="color:cyan">The color associated with CH-A is cyan if it is currently selected.</span>
* V2 <span style="color:cyan">The color associated with CH-A is cyan if it is currently selected.</span>
* T1 <span style="color:brown">The color associated with synchronous mode is brown since this is related.</span>
* T2 <span style="color:brown">The color associated with synchronous mode is brown since this is related.</span>
* Y <span style="color:cyan">The color associated with CH-A is cyan if it is currently selected.</span>
* X <span style="color:brown">The color associated with synchronous mode is brown since this is related.</span>
* T0 <span style="color:brown">The color associated with synchronous mode is brown since this is related.</span>
* 4K <span style="color:brown">The color associated with synchronous mode is brown since this is related.</span>
* EXT <span style="color:white">The color associated with EXT is white since this is otherwise unrelated to the other color codes seen.</span>

#### Bottom display-only data
The values seen here are not menu items and may not be selected. These are usually the result of setting up on-screen V1/V2/T1/T2 references to measure signals. Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently.
* ΔV: +4.80V <span style="color:cyan">The color associated with CH-A is cyan if it is currently selected.</span>
* ΔT: +133 µS <span style="color:brown">The color associated with synchronous mode is brown since this is related.</span>
* Vbt +4.15V 

#### On-screen indicators and markers
* T: Horizontal line for the trigger voltage associated with either CH-A or CH-B, depending upon its associated color
* 1: The CH-A waveform, if shown  <span style="color:cyan">The color associated with CH-A is cyan.</span>
* 2: The CH-B waveform, if shown  <span style="color:yellow">The color associated with CH-B is yellow.</span>
* 3: The CH-C waveform, if shown  <span style="color:purple">The color associated with CH-C is purple.</span>
* 4: The CH-D waveform, if shown  <span style="color:green">The color associated with CH-D is green.</span>
* Unmarked vertical line: The marker associated with the T1 reference, useful for measuring the ΔT of one cycle of the waveform when in the HOLD position, for example
* Unmarked vertical line: The marker associated with the T2 reference, useful for measuring the ΔT of one cycle of the waveform when in the HOLD position, for example
* Unmarked vertical line: The marker associated with the T0 reference
* Unmarked horizontal lines in the background grid pattern: Useful for estimating voltages

#### Popup Values Detail (from K3 toggle)
Here, I just indicate what I'm seeing currently on my screen based upon the prior selections I made, noting that yours may show differently.
* Vbt +3.98V  (battery voltage) <span style="color:purple">The color associated with this is purple.</span>
* FRQ -----  (signal frequency) <span style="color:purple">The color associated with this is purple.</span>
* CIR 0.000nS  (signal cycle) <span style="color:purple">The color associated with this is purple.</span>
* DUT 0.000%  (duty factor) <span style="color:purple">The color associated with this is purple.</span>
* TH 0.000nS  (Monocycle high-level time) <span style="color:yellow">The color associated with this is cyan.</span>
* TL 0.000nS  (Monocycle low-level time) <span style="color:yellow">The color associated with this is yellow.</span>
* Vpp +200 mV  (peak-to-peak voltage) <span style="color:cyan">The color associated with this is cyan.</span>
* Vdc +160 mV  (direct current voltage) <span style="color:cyan">The color associated with this is cyan.</span>

#### Popup Menu (from K2 toggle)
* Save Param (Use NAV-B to select this option and then PUSH NAV-A to perform this function)
* Save Dat
* Save Buf
* Save Bmp
* Save Csv
* Load Dat
* Load Buf
* BackLight (Use NAV-B to select this option then left/right on NAV-A to change)
* Buzzer (Volume control: Use NAV-B to select this option then left/right on NAV-A to change)
* Standby (Minutes until screen is blacked, similar selection as above)
* Calibrat
