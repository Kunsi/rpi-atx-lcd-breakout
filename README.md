# RPi-ATX-LCD-Breakout

This board allows you to connect an ATX power supply and a HD44780-comptible LCD
screen to your Raspberry Pi (or others with compatible GPIO layout).

While it does have a 40pin GPIO connector, it will also work with older 
26-pin variants of the Pi.

The board was created to provide a convenient interface for two
[Octoprint](http://octoprint.org/) plugins: PSUControl and LCD-HD44780 (See
links on bottom of this page).

![Board](img/top.jpg?raw=true)

The board itself offers a variety of features:
* Powering the Pi using +5VSB (standby power)
* Switching the PSU on and off using GPIO Pin 12
  
  The GPIO pin can be connected to PS_ON directly, or via a transistor. This is
  choosable using the three-pin jumper switch.

  Alternatively, the PSU can be forced to be on, by using the 2-pin PS_ON
  jumper.
* Connecting a character LCD to the Pi
  
  LCD is wired as follows:
  <dl>
    <dt>Register Select</dt>
    <dd>15</dd>

    <dt>Enable</dt>
    <dd>16</dd>

    <dt>Data 4</dt>
    <dd>21</dd>

    <dt>Data 5</dt>
    <dd>22</dd>

    <dt>Data 6</dt>
    <dd>23</dd>

    <dt>Data 7</dt>
    <dd>24</dd>
  </dl>

  Data 0-3 pins are not connected. Read/Write select has been wired to GND, so
  it's not possible to read data from the LCD screen. Contrast pin is
  connected to a potentiometer.
* Allow connecting of two fans, one 5V, one 12V
* Providing screw terminals for GND, +12V, +5VSB and +5V
* Providing a USB outlet powered by +5VSB

Note: All pin numbers use BOARD numbering.

## Cost
Prices are in Euro, and are based on my prototype production cost

Item            | Count    | Price | Link
----------------|---------:|------:|---
PCB             | 1        | 1.70  | [PCBway](https://www.pcbway.com/) got me 10 boards for 17$
Fan connector   | 2        | 0.42  | <https://www.reichelt.de/?ARTICLE=185658>
Pin header      | 3+2 wide | 0.09  | <https://www.reichelt.de/?ARTICLE=119891>
Potentiometer   | 1        | 0.38  | <https://www.reichelt.de/?ARTICLE=14951>
LCD connector   | 1        | 0.52  | <https://www.reichelt.de/?ARTICLE=175351>
Screw terminals | 2        | 0.42  | <https://www.reichelt.de/?ARTICLE=170222>
Jumper          | 1        | 0.03  | <https://www.reichelt.de/?ARTICLE=119944>
USB connector   | 1        | 0.20  | <https://www.reichelt.de/?ARTICLE=22184>
Transistor      | 1        | 0.09  | <https://www.reichelt.de/?ARTICLE=1999>
>esistors       | 1+1+1    | 0.30  | <https://www.reichelt.de/?ARTICLE=1381><br> <https://www.reichelt.de/?ARTICLE=1315><br> <https://www.reichelt.de/?ARTICLE=1338>
GPIO connector  | 1        | 0.11  | [https://de.aliexpress.com/…/32454935478.html](https://de.aliexpress.com/item/100pcs-lot-2-54mm-Double-Row-Female-12P-Straight-Header-Pitch-Socket-Strip-2X20-Pin/32454935478.html)
ATX connector   | 1        | 0.43  | <http://www.mouser.de/ProductDetail/TE-Connectivity/1-1775099-3/>

## Links
* [OctoPrint-PSUControl](https://github.com/kantlivelong/OctoPrint-PSUControl) by kantlivelong
* [Octoprint-LCD-HD44780](https://github.com/Kunsi/Octoprint-LCD-HD44780) by Kunsi
