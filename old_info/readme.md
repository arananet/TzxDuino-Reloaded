This folder contains the old information about version 1.4.

# TzxDuino-Reloaded 1.4

Based on the original design of Andrew Beer, Duncan Edwards.

This new version has been completely reworked with smd components. Also change the distribution and connection orientation. Now, you just plug the TzxDuino on the Spectrum jack and use a common Android power supply (microusb b) and that's it, start loading tzx files!. This design also allows to use every type of i2c LCD or OLED Screen, by soldering a 1x4 row pin and taking out the lcd to a better viewable area.

# Works with

- TZX, TAP (Spectrum)
- TSX, CAS (MSX)
- CDT (AMSTRAD)

# Audio Amp

Since is not very clear if there is necessary a output amp, I have added a little DPDT, one position switch to bypass or enable the D9 signal to the AMP LM386. The other position will connect the D9 signal directly to the 3.5mm jack. 

Update 26-10-2018. There is a small bug on the PCB for the OP AMP. Hopefully Antonio Villena has sorted out. The trick is this:

1-You must short (with a solder bolb) C3, R4, R5.
2-You must short two pins of the selector (s1). Check images below.

<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/fix1.jpg?raw=true" width="700">
<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/fix2.jpg?raw=true" width="700">

Thanks Antonio.

# Images

<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/top1.png?raw=true" width="700">

<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/bottom1.png?raw=true" width="700">

# Instructions
 
1. Download the official TzxDuino code from http://arduitapemarkii.blogspot.com.es/2017/06/tzxduino-17.html or you can also use the Maxduino Firmware from RCMOLINA https://github.com/rcmolina/MaxDuino_v1.53.
2. Set the display hardware address on the TZXDuino_V1.7b.ino or the MaxDuino_v1.53.ino depending on what kind of display have. If does not work, use a i2c scanner in order to get the exact hardware address from the display.
3. Use a serial TTL programmer and the Arduino IDE to upload the code into the ATMEGA.
4. Plug an MicroSD card with all the files and enjoy the power of the TzxDuino!
5. In case we use the hex file to clon and flash many TzxDuino devices we need to set the fuses with the avrdude. 

Fuses are lfuse = 0xff hfuse = 0xDA, efuse = 0x05, LB = 0x0F

# Acrylic case

I also made an acrylic case for this pcb. https://www.thingiverse.com/thing:2535743 (not updated for version 1.4 yet)

# Updates

18/11/2019: Added link to the MAXDUINO firmware.

12/11/2019: Updated license stuff (I usually not do this but I must start it with this).

23/04/2018: Fix some issues with the op amp, adding two resistors (jgilcas). Removed the solder jumper and the spst switch and change both with an DPDT switch (A.Villena). Changed the orientation of the external connection to make it compatible with the SUGARLESS project (spark2k06).

Bom updated.

17/02/2018: Add a screen voltage selector, this is because some chinese oled screen came with the VCC and GND mixed. This can be change on the screen (there are two resistros to swap voltage) but it will more fast to select onboard with two new available solder jumpers.

Changed the USB connector to a most common used.

20/01/2018: Mayor update:

* Fix silkscreen components.
* Added a gain regulator (if the op amp is present) by @jgilcas.
* Added a on-off switch for the op amp proposed by @jgilcas.
* Added a 5x2 pcb connector for use with other devices, proposed by spark2k06.
* Bom updated.
* Acrylic case updated.

18/12/2017: Bom updated. (thanks to @jgilcas for the tips)

03/11/2017: Complete redesigned for use with arduino pro mini.

16/09/2017: Added a 2.5mm for use with remote signal (MSX) and a DTR signal. Components realocated.

06/09/2017: Added a SD card socket on the back. You must cut the jack 3.5mm pins that are too large.

06/09/2017: First initial release. 

# Bill of materials

| Part          | Value                   | Package                        |
| ------------- | ----------------------- | ------------------------------ | 
| C1            | 10uf/22uf               | C0805K                         |
| C2            | 10uf/22uf               | C0805K                         |
| C3            | 0.22uF                  | C0805K                         |
| C4            | 10uf                    | C0805K                         |
| C5            | 220uf (ECA-0JM221)      | CPOL-EUE1.8-4 (only with amp)  |
| M2            | ARDUINO PRO MINI        | PCB                            |
| REG           | LM1117 3V3              | SOT223                         |
| IC1           | 4050D                   | SO16                           |
| IC4           | LM386M-1                | SO08 (only if amp required)    |
| ISP           | AVR_SPI_PRG_6PTH        | 2X3                            |
| TTL           | PINHD_1X04              | 1X04                           |
| JP1           | OLED SCREEN CONNECTOR   | 1X04_ROUND                     |
| K1            | MICROUSB B              | 629105136821                   |
| POWER         | SMD 0805 LED            | CHIP-LED0805                   |
| ACT           | SMD 0805 LED            | CHIP-LED0805                   |
| R1            | 10K TrimPotentiometer   | RTRIM3103   (only with amp)    |
| R2 (FOR LED)  | 330/560/1K              | R0805                          |
| R3 (FOR LED)  | 330/560/1K              | R0805                          |
| R4            | 10K                     | R0805 (only with amp)          |
| R5            | 10K                     | R0805 (only with amp)          |
| PLAY          | PUSH BUTTON             | B3F-31XX                       |
| DOWN          | PUSH BUTTON             | B3F-31XX                       |
| ROOT          | PUSH BUTTON             | B3F-31XX                       |
| STOP          | PUSH BUTTON             | B3F-31XX                       |
| UP            | PUSH BUTTON             | B3F-31XX                       |
| SD1           | MicroSD socket          | TF-PULL                        |
| SD SOCKET     | SDCARD_SMT_4U06132      | SDCARD_SMT_4U06132             |
| X1            | STEREOJACK 3.5mm        | STX3100                        |
| X2            | STEREOJACK 2.5mm        | PJ-204B                        |
| X3            | 5X2 Pin row             | Standard 1" double pin row     |
| S1            | DPDT Switch             | AYZ0202                        |

This is the arduino used in all the versions of the TZXDUINO. Must have A4 and A5 at bottom of the A2 and A3. AliExpress Link. https://es.aliexpress.com/store/product/Free-Shipping-New-Atmega328-5v-Version-Pro-Mini-Module-16M-For-Arduino-Compatible/1962508_32605434250.html?spm=a219c.search0104.3.6.27c06b16t4pHKf&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10065_5722813_10151_10344_10068_10342_5722613_10547_10343_5722913_10340_10341_10548_10698_10697_10696_10084_10083_5722713_10618_10307_10301_10303_5711213_10059_10184_10534_308_100031_10103_441_10624_10623_10622_10621_10620_5722513_5711313,searchweb201603_1,ppcSwitch_5&algo_expid=69227fd3-b92f-4d61-afc6-97915d0331e3-3&algo_pvid=69227fd3-b92f-4d61-afc6-97915d0331e3&transAbTest=ae803_1&priceBeautifyAB=0

This are the DPDT switches that are maybe compatible with the footprint:

https://es.aliexpress.com/store/product/70pcs-On-Off-On-6-Pin-DPDT-Vertical-Mini-SMD-SMT-Slide-Power-Switch-7x6x4mm/1178755_1953364266.html?spm=a219c.search0104.3.146.287176b1h1eqtT&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10065_5722813_10151_10344_10068_10342_5722613_10547_10343_5722913_10340_10341_10548_10698_10697_10696_10084_10083_5722713_10618_10307_10301_10303_5711213_10059_10184_308_100031_10103_441_10624_10623_10622_10621_10620_5722513_5711313,searchweb201603_15,ppcSwitch_5&algo_expid=6e95ecf1-40f5-4b5b-8649-c467855a15c0-22&algo_pvid=6e95ecf1-40f5-4b5b-8649-c467855a15c0&transAbTest=ae803_1&priceBeautifyAB=0

# Note

This is a work in progress, several testing must be made but it should work as is. I take no responsibiltiy for any damage to any equipment that results from the use of this board. USE AT YOUR OWN RISK!

If you like the project or want to support it, you can buy me a beer or a KO-FI :) 
[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/H2H51MPWG)

# License

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0
International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

