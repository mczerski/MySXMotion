# MySXMotion
## MySX Board for motion sensor

This is a multipurpose daughterboard but its main use is for AS312 motion sensor with MySX conector. It also consist of BH1750 ambient light sensor and header for one i2c device, uart and avr ISP. It is meant to be combined with a [MySMotherboard] (https://www.openhardware.io/view/606/MySMotherboard) to make fully functional motion sensor node.

<img src="https://raw.githubusercontent.com/mczerski/MySXMotion/master/img/IMG_20180708_110438.jpg">

## Features:

1. support for SMD MySX header for low profile connection with MySX motherboard
2. AS312 motion sensor with dedicated LDO
3. BH1750 ambient light sensor
4. I2C header
5. AVR ISP header
6. uart header

## HOW TO
1. Low profile MySX header connector.
The board is designed for smd low profile MySX 2.5 header connector which significantly reduces node size. 
<img src="https://raw.githubusercontent.com/mczerski/MySXMotion/master/img/IMG_20180707_142805.jpg">

2. AS312 motion sensor
For best performance motion sensor is powered through dedicated low quiescent current 3V LDO. The LDO is powered from MySX VRAW pin, so voltage on this pin must be higer than 3.1V. 3.7V LI-ION rechargable battery would be a good power source solution. The circuit consists also of battery reverse polarity protecion MOSFET.
For motion sensor required components to solder are:
Q1, C1, C2, C3, R1, IC1, IC3

3. BH1750 ambient light sensor
Ambient light sensor is powered from the MySX VCC pin. J2 jumper is used to select I2C addres of the light sensor.
Required components to solder are:
R2, R3, R4, C4, C5, IC2, J1 (choose one of two options)

4. Additional headers
By soldering ISP header this board can be use as a MySX to AVR ISP adapter. To I2C header one additional i2c device can be conected. To UART header one additional uart device can be connected.
