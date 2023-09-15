bledstripper-grove
==================

Bluetooth Low Energy LED strip controller circuit board with standard Grove connectors.  Open hardware under the MIT License.


Overview
--------

The __bledstripper-grove__ combines a MDBT42Q Bluetooth Low Energy SoM and four Grove connectors that can be driven with high-amperage 5VDC power via a standard barrel connector.  It simplifies the wireless programming and control of up to four long strips of WS2813 LEDs (or equivalent).

![bledstripper-grove render](https://reelyactive.github.io/bledstripper-grove/images/bledstripper-grove-render-230317.png)


LED Strips
----------

The __bledstripper-grove__ is designed to offer plug-and-play compatibility with [Seeed Studio's family of WS2813 LED strips](https://www.seeedstudio.com/Grove-WS2813-RGB-LED-Strip-Waterproof-30-LED-m-1m.html) which use standard Grove connectors.  The __bledstripper-grove__ is nonetheless compatible with the family of 5VDC addressable LEDs commonly referred to as NeoPixels, strips of which can alternatively be directly soldered to the through-hole connectors of J1-J4 of the board.


Schematic
---------

![bledstripper-grove schematic](https://reelyactive.github.io/bledstripper-grove/images/bledstripper-grove-schematic-230317.png)


Key components
--------------

The __bledstripper-grove__ comprises the following three key components:
- [Raytac's MDBT42Q-512KV2 module](https://www.raytac.com/product/ins.php?index_id=31), which is based on the Nordic nRF52832 Bluetooth Low Energy IC, and which is [Espruino](https://www.espruino.com/MDBT42Q)-compatible.
- [TI's LP2985-33DBVR](https://www.ti.com/product/LP2985) 3.3V low-dropout voltage regulator to power the MDBT42Q
- [TI's TXU0104QPWRQ1](https://www.ti.com/product/TXU0104) four-channel voltage-level translator to convert the high-speed LED control signals from 3.3V to 5.0V

BOM selection was made to maximise [Shenzhen/Seeed OPL](https://www.seeedstudio.com/opl.html) (open parts library) components which include:

| Part number           | Shenzhen OPL SKU | Description   |
|:----------------------|:-----------------|---------------|
| MDBT42Q-512KV2        | 317030213        | E1 (SoC)      |
| LP2985-33DBVR         | 310030033        | U3 (LDO)      |
| 19-217-R6C-AL1M2VY-3T | 304090042        | D1 (Red)      |
| 19-217-BHC-ZL1M2RY-3T | 304090045        | D2 (Blue)     |
| 19-217-G7C-AN1P2-3T   | 304090043        | D3 (Green)    |
| 1125R-4P              | 320110034        | J1-J4 (Grove) |


MDBT42Q Pins
------------

| Function      | MDBT42Q Pin | nRF52832 Pin | Espruino Pin |
|:--------------|:------------|:-------------|:-------------|
| Red LED       | 16          | P0.3         | D3           |
| Blue LED      | 17          | P0.4         | D4           |
| Green LED     | 18          | P0.5         | D5           |
| Output Enable | 23          | P0.10        | D10          |
| LED data CH1  | 26          | P0.12        | D12          |
| LED data CH2  | 27          | P0.13        | D13          |
| LED data CH3  | 28          | P0.14        | D14          |
| LED data CH4  | 29          | P0.15        | D15          |


Enclosure
---------

The __bledstripper-grove__ is designed to fit the inexpensive [Hammond Manufacturing 1551K enclosure](https://www.hammfg.com/electronics/small-case/plastic/1551), which is available with or without flange, and in several colours.  Cutouts are required for the barrel connector and grove connectors.


Project History
---------------

The __bledstripper-grove__ is a collaboration between [reelyActive](https://www.reelyactive.com/) and [génielab.](https://genielab.co/), with the v0.1 layout completed by [TristanFranc](https://github.com/TristanFranc/).


License
-------

MIT License

Copyright (c) 2023 [reelyActive](https://www.reelyactive.com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN 
THE SOFTWARE.