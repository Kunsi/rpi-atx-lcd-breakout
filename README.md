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

## Links
* [OctoPrint-PSUControl](https://github.com/kantlivelong/OctoPrint-PSUControl) by kantlivelong
* [Octoprint-LCD-HD44780](https://github.com/Kunsi/Octoprint-LCD-HD44780) by Kunsi
