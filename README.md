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
