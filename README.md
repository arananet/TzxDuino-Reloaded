# TzxDuino-Reloaded

Based on the original design of Andrew Beer, Duncan Edwards.

This new version has been completely reworked with smd components. Also change the distribution and connection orientation. Now, you just plug the TzxDuino on the Spectrum jack and use a common Android power supply (microusb b) and that's it, start loading tzx files!. This design also allows to use every type of i2c LCD or OLED Screen, by soldering a 1x4 row pin and taking out the lcd to a better viewable area.

# Note

This is a work in progress, several testing must be made but it should work as is. I take no responsibiltiy for any damage to any equipment that results from the use of this board. USE AT YOUR OWN RISK!

# Audio Amp

Since is not clear if there is necessary a output amp, I have added a little solder jumper to enable or disable the AMP LM386. By setting the jumper to 1-2, will use the op amp onboard (if you solder the lm386 on the pcb). Else if we don't want to use he AMP, we can set the jumper to 2-3, this will connect the D9 signal directly to the 3.5mm jack.

# Images

<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/top.png?raw=true" width="700">

<img src="https://github.com/arananet/TzxDuino-Reloaded/blob/master/images/bottom.png?raw=true" width="700">

# Instructions
 
1. Download the official TzxDuino code from http://arduitapemarkii.blogspot.com.es/2017/06/tzxduino-17.html 
2. Set the display hardware address on the TZXDuino_V1.7b.ino depending on what kind of display have. If does not work, use a i2c scanner in order to get the exact hardware address from the display.
3. Use a serial TTL programmer and the Arduino IDE to upload the code into the ATMEGA.
4. Plug an MicroSD card with all the files and enjoy the power of the TzxDuino!
5. In case we use the hex file to clon and flash many TzxDuino devices we need to set the fuses with the avrdude. Fuses are lfuse = 0xff
hfuse = 0xde, efuse = 0x05

# Updates

06/09/2017: Added a SD card socket on the back. You must cut the jack 3.5mm pins that are too large.
06/09/2017: First initial release. 

# Bill of materials

| Part          | Value                   | Package                        |
| ------------- | ----------------------- | ------------------------------ | 
| C2            | 0.1uF                   | C0805K                         |
| C3            | 0.22uF                  | C0805K                         |
| C4            | 220uf                   | 153CLV-0605                    |
| C5            | 10uf                    | C0805K                         |
| C13           | 22p                     | C0805                          |
| C14           | 22p                     | C0805                          |
| IC1           | 4050D                   | SO16                           |
| IC2           | AVR-ATMEGA328p-TQP32    | QFP32                          |
| IC3           | LP298XS                 | SOT23-5L                       |
| IC4           | LM386M-1                | SO08                           |
| ISP           | AVR_SPI_PRG_6PTH        | 2X3                            |
| J1            | LM386 yes/no            | JP3_0805                       |
| JP1           | OLED SCREEN CONNECTOR   | 1X04_ROUND                     |
| K1            | MICROUSB B              | 629105136821                   |
| POWER         | SMD 0805 LED            | CHIP-LED0805                   |
| ACT           | SMD 0805 LED            | CHIP-LED0805                   |
| Q3            | 16MHZ                   | QS                             |
| R6            | 10k                     | R0805                          |
| R7            | 120                     | R0805                          |
| R8            | 1M                      | R0805                          |
| R9            | 1K                      | R0805                          |
| PLAY          | PUSH BUTTON             | B3F-31XX                       |
| DOWN          | PUSH BUTTON             | B3F-31XX                       |
| ROOT          | PUSH BUTTON             | B3F-31XX                       |
| S1            | PUSH BUTTON             | B3F-10XX                       |
| STOP          | PUSH BUTTON             | B3F-31XX                       |
| UP            | PUSH BUTTON             | B3F-31XX                       |
| SD1           | TF-HOLDER               | TF-PULL                        |
| TTL           | PINHD_1X03              | 1X03                           |
| X1            | STEREOJACK              | STX3100                        |
| SD SOCKET     | SDCARD_SMT_4U06132      | SDCARD_SMT_4U06132             |
