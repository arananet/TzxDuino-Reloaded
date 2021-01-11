# TzxDuino-Reloaded 1.5 Nano

Based on the original design of Andrew Beer, Duncan Edwards.

This new version has been completely reworked with smd components. Also change the distribution and connection orientation. Now, you just plug the TzxDuino on the Spectrum jack and use a common Android power supply (microusb b) and that's it, start loading tzx files!. 

# Coworkers

I would like to thanks to the people that have helped these years on fix things of this project and also for extra tips to improve it. These people are well know on the retrocommunity in general: @jgilcas, spark2k06, Antonio Villena and Noel Llopis.

# Works with

- TZX, TAP (Spectrum)
- TSX, CAS (MSX)
- CDT (AMSTRAD)

# Audio Amp

Since is not very clear if there is necessary a output amp, I have added a little DPDT, one position switch to bypass or enable the D9 signal to the AMP LM386. The other position will connect the D9 signal directly to the 3.5mm jack. If the volume of the output is higher than expected you can change the value of the R5 resistor from 1k to 10k.

# Images

<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/tzxduino_reloaded_nano1.png?raw=true" width="700">

<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/tzxduino_reloaded_nano_back.png?raw=true" width="700">

# Instructions
 
1. Download the official TzxDuino code from http://arduitapemarkii.blogspot.com.es/2017/06/tzxduino-17.html or you can also use the Maxduino Firmware from RCMOLINA https://github.com/rcmolina/MaxDuino_v1.53.
2. Set the display hardware address on the TZXDuino_V1.7b.ino or the MaxDuino_v1.53.ino depending on what kind of display have. If does not work, use a i2c scanner in order to get the exact hardware address from the display.
3. Upload the firmware code using the Arduino IDE.
4. Plug an MicroSD card with all the files and enjoy the power of the TzxDuino! 

# Acrylic case

I've update the acrylic case for this new version, it's available here: https://www.thingiverse.com/thing:2535743, you can use the services of transparentcitysales@gmail.com so they can cut the design in acrylic.

# Updates

11/01/2021: New version 1.5 Nano, reworked with all the fixes. I've changed the Arduino Pro mini for a Arduino Nano for an easy programming and firmware update and also because since the Nano includes some components that was on the old version, it helps to simplify the design. Also remove the SD socket because in nowdays is useless. Bom Updated for the new version. Old version is on the old_info directory. All the changes has been removed from this readme. Also now you can use two types of oled displays, 128x64 or 128x32.

06/09/2017: First initial release. 

# Bill of materials for 1.5 Nano

| Part          | Value                   | Package                        |
| ------------- | ----------------------- | ------------------------------ |
| ACT	        | RED	                  | CHIP-LED0805                   | 
| C1	        | 100nf	                  | C0805                          |
| C2	        | 100nf	                  | C0805                          |
| C3	        | 10uf	                  | C0805                          |
| C4	        | 47nf	                  | C0805                          |
| C6	        | 100nf	                  | C0805                          |
| C5            | 220uf (ECA-0JM221)      | CPOL-EUE1.8-4 (only with amp)  |
| IC1	        | 4050D	                  | SO16                           |
| IC4	        | LM386M-1	              | SO08 (only if amp required)    |
| POWER	        | GREEN	                  | CHIP-LED0805                   |
| PWR	        | MICRO-USB-B             | MICRO_USB_4_LEGS               |
| R1	        | 10	                  | R0805                          |
| R3	        | 330	                  | R0805                          |
| R3	        | 330	                  | R0805                          |
| R5	        | 1k	                  | R0805 (adjust to your needs)    |
| S1	        | SWITCH-DPDTSMD	      | AYZ0202                        |
| SD1	        | TF-HOLDER	              | TF-PULL                        |
| X1            | STEREOJACK 3.5mm        | STX3100                        |
| X2            | STEREOJACK 2.5mm        | PJ-204B                        |
| PLAY          | PUSH BUTTON             | B3F-31XX                       |
| DOWN          | PUSH BUTTON             | B3F-31XX                       |
| ROOT          | PUSH BUTTON             | B3F-31XX                       |
| STOP          | PUSH BUTTON             | B3F-31XX                       |
| UP            | PUSH BUTTON             | B3F-31XX                       |
| M1            | ARDUINO NANO            | SEE LINK BELOW                 |

# External parts

Arduino Nano

This is the arduino used on the new version 1.5 https://es.aliexpress.com/item/1005001706390728.html?spm=a2g0o.productlist.0.0.22ae1b61xzGZdn&algo_pvid=6e84573f-72f2-408d-8187-1859f93df6f0&algo_expid=6e84573f-72f2-408d-8187-1859f93df6f0-0&btsid=2100bddb16103571535116853eaf9c&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_

This are the DPDT switches that are maybe compatible with the footprint:

https://es.aliexpress.com/store/product/70pcs-On-Off-On-6-Pin-DPDT-Vertical-Mini-SMD-SMT-Slide-Power-Switch-7x6x4mm/1178755_1953364266.html?spm=a219c.search0104.3.146.287176b1h1eqtT&ws_ab_test=searchweb0_0,searchweb201602_4_10152_10065_5722813_10151_10344_10068_10342_5722613_10547_10343_5722913_10340_10341_10548_10698_10697_10696_10084_10083_5722713_10618_10307_10301_10303_5711213_10059_10184_308_100031_10103_441_10624_10623_10622_10621_10620_5722513_5711313,searchweb201603_15,ppcSwitch_5&algo_expid=6e95ecf1-40f5-4b5b-8649-c467855a15c0-22&algo_pvid=6e95ecf1-40f5-4b5b-8649-c467855a15c0&transAbTest=ae803_1&priceBeautifyAB=0

Usb connector

https://lcsc.com/product-detail/USB-Connectors_SHOU-HAN-MICRO-4P-DIP_C456008.html

# Oled display

Note that with the new version 1.5, now you can use oled displays types of 128x64 or 128x32 versions but the pins must be in this order: GND VCC SCL SDA.

# Note

This is a work in progress, several testing must be made but it should work as is. I take no responsibiltiy for any damage to any equipment that results from the use of this board. USE AT YOUR OWN RISK!

If you like the project or want to support it, you can buy me a beer or a KO-FI :) 
[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/H2H51MPWG)

# License

ATTENTION: This is for ebay sellers, this project was made for the retro community and not for resale on ebay. So only retro hardware forums and individual person can build this project. ITS NOT FOR EBAY SALE.

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0
International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
