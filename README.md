Edison WiFi Car
===============

To build WiFi Car with Intel Edison and Seeed Skeleton Bot.

![](www/img/car_top_view.jpg)

## Hardware
+ Intel Edison + Edison Arduino Breakout
+ [Skeleton Bot](http://www.seeedstudio.com/wiki/Skeleton_Bot_-_4WD_hercules_mobile_robotic_platform)
+ [Grove - I2C Motor Driver](http://www.seeedstudio.com/wiki/Grove_-_I2C_Motor_Driver_V1.3)
+ [Base Shield](http://www.seeedstudio.com/wiki/index.php?title=Base_shield_v2&uselang=en)

[https://files.seeedstudio.com/wiki/Edison_4WD_Auto_Robotic_Platform_2.0/res/Parts_List_for_Intel_Edison.pdf](https://files.seeedstudio.com/wiki/Edison_4WD_Auto_Robotic_Platform_2.0/res/Parts_List_for_Intel_Edison.pdf)

Connect the Grove - I2C Motor Driver to Base Shield's A0 Grove connector (A0 - SCL, A1 - SDA).

## Software
### Requirements
+ libmraa0 (tested with v0.5.4)

### Usage
Download this repository to Edison and run:
```
cd {REPO_DIR}
./run.sh
```
Connect to the Edison WiFi network and open 192.168.42.1 in your web browser.

### Create an ipk
Just run `make`, wificar.ipk will be created.
Then copy wificar.ipk to Edison and run:
```
opkg install wificar.ipk
systemctl start wificar.service   # start wificar
systemctl enable wificar.service  # autorun wificar at startup
```

## To Do
- [ ] Communication protocol uses WebSocket to replace HTTP GET
- [ ] Add Camera


## Parts:

 

- Parts Description   Qty. 
- PCB Assembly‐4WD Driver Platform V1.0  1 
- Long Aluminum Board(left);L230*W40*H20*D3.0mm  1 
- Long Aluminum Board(right);L160*W40*H20*3.0mm  1 
- Bracket;L29*W12*2.0mm  4 
- Top Plate L200*W132*1.5mm  1 
- PMMA Fixingboard‐L236*W20*H3.0mm  1 
- Black PMMA Upper Board‐L214*W159.36*H3.0mm  1 
- Shaft Coupling;Ф4mm*W12mm*L22mm‐Silver  4 
- DC Motor;D25*H51.8+26mm  4 
- Distance Spacer‐M3.0*H45+6.0mm  4 
- Distance Spacer;M3*10mm  4 
- Distance Spacer;M2*10mm  12 
- Flat Head Socket Cap Screw‐KM4.0*H8.0mm  16 
- Cross Recessed Round Head Screw‐PM4.0*H8.0mm  4 
- Cross Recessed Washer Head Screw‐PM3.0*H8.0mm  12 
- Cross Recessed Pan Washer Head Screw‐PWM3.0*H6.0mm  20 
- Phillips Pan Head Screws With Two Washer M2*8mm   24 
- Nut;Silver‐M3.0*H2.5mm  4 
- Split Washer;Silver‐OD7*ID4*H1mm  4 
- Screw Driver;M2.5*L53mm  1 
- Nut;Sliver‐M4.0*3.2mm  4 
- Manual  1 
- Velcro Tape;20mm*220mm  1 
- Wheel;110mm*45.6mm  4 
- Nylon Hinge;40*30.5mm  2 
- Plate Spanner;8mm  1 
- Black PMMA Bottom Boardv2；L236*W138*H3.0mm‐激光加工  1 
- Cross Recessed Round Head Screw， M3*6mm  3 
- Cross Recessed Flat Head Screw；KM4.0*10.0mm  8 
- Power Cable;22AWG‐310mm‐Black  1 
- Jumper Black;2P‐2.54‐Short  1 
- Heat Sink‐20*15*6mm  4 
- Plate Spanner‐7mm  1 
- Philips Screw Driver;M6*L211mm‐Yellow/Black  1 
- Philips Screw Driver;M3*L155mm‐Yellow/Black  1 
 
 
 
## PIN Mappings


 
- PIN  Name  Function  PIN  Name  Function 
- 1  GND    70  GP81  Motor A EN(Motor En & Disable)
- 2  VSYS    69  FW_RCVR    
- 3  USB_ID    68  GP83  Motor A IN1(Direction control1) 
- 4  VSYS    67  CLK_OUT    
- 5  GND    66  GP80  Motor A IN2(Direction control2)
- 6  VSYS    65  GP128  Motor B EN(Motor En & Disable)
- 7  MSIC    64  GP82  Motor B IN1(Direction control1) 
- 8  3.3V    63  GP129  Motor B IN2(Direction control2)
- 9  GND    62  GP79  Motor C IN2(Direction control2)
- 10  3.3V    61  GP130  UART1_RX 
- 11  GND    60  GP77    
- 12  1.8V    59  GP114  SPI2_MISO 
- 13  GND    58  GP78  Motor A SIG2(Encoder input B) 
- 14  DCIN    57  GP115  SPI2_MOSI 
- 15  GND    56  GP43    
- 16  USB_DP    55  GP109  SPI2_CLK 
- 17  PWRBTN    54  GP41  Motor B SIG1(Encoder input A) 
- 18  USB_DN    53  GP110  Motor A SIG1(Encoder input A) 
- 19  FALUT    52  GP40  Motor B SIG2(Encoder input B) 
- 20  USB_VBUS    51  GP111  SPI2_CS2 
- 21  PSW    50  GP42  ADC_RDY 
- 22  GP134  UART2_RX  49  UNUSED    
- 23  V_VBAT    48  GP14  Motor D SIG1(Encoder input A) 
- 24  GP44  Motor D EN(Motor En & 
- Disable)  47  GP28  I2C6_SDA 
- 25  GP165  Motor D IN1(Direction control1)  46  GP131  UART1_TX 
- 26  GP45  Motor D IN2(Direction control2) 45  GP27  I2C6_SCL 
- 27  GP135  UART2_TX  44  GP84  Motor D SIG2(Encoder input B) 
- 28  GP46  Motor C EN(Motor En & Disable) 43  GP20  I2C1_SDA 
- 29  UNUSED    42  GP15  Motor C SIG1(Encoder input A) 
- 30  GP47  Motor C IN1(Direction control1)  41  GP19  I2C1_SCL 
- 31  PCVR_MODE    40  UNUSED    
- 32  GP48  DO NOT USE  39  GP183_PWM
- 3  Motor A PWM(Speed control) 
- 33  GP13_PWM
- 1  Motor D PWM(Speed control)  38  UNUSED    
- 34  GP49  Motor C SIG2(Encoder input B)  37  GP182_PWM
- 2  Motor B PWM(Speed control) 
- 35  GP12_PWM
- 0  Motor C PWM(Speed control)  36  REST_OUT  Motor A EN(Motor En & Disable)

 
----

This software in this repository is written by [Seeedstudio](http://seeed.cc)<br>
and is licensed under [The MIT License](http://opensource.org/licenses/MIT).

Contributing to this software is warmly welcomed. You can do this basically by<br>
[forking](https://help.github.com/articles/fork-a-repo), committing modifications and then [pulling requests](https://help.github.com/articles/using-pull-requests) (follow the links above<br>
for operating guide). Adding change log and your contact into file header is encouraged.<br>
Thanks for your contribution.

Seeed Studio is an open hardware facilitation company based in Shenzhen, China. <br>
Benefiting from local manufacture power and convenient global logistic system, <br>
we integrate resources to serve new era of innovation. Seeed also works with <br>
global distributors and partners to push open hardware movement.<br>

[![Analytics](https://ga-beacon.appspot.com/UA-46589105-3/Edison_WiFi_Car)](https://github.com/igrigorik/ga-beacon)
