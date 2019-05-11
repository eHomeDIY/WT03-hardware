# WT03-hardware

Schematic and PCB design files for the project.

They are generated with EasyEDA.

Some notes regarding the designs:

~~The diode D1's package was larger than in the design, additional drilling will be needed for it to fit. Will be corrected in a future revision~~
Corrected in v1.1

~~The ground plane for the regulator U4 is a slight overkill, will be corrected in a future revision.~~
Corrected in v1.1

~~Mounting holes are also larger than required for the used enclosure. Will be corrected in a future revision.~~
Corrected in v1.1

~~Actual size of the PCB is 55mm x 67mm which is a little bit larger than the required for the enclosure but it still fits. Will be corrected in a future revision.~~
Corrected in v1.1

The exposed copper area to the right of the ESP-01 is connected to the RESET pin of the ESP.

Some components used which are not mentioned in the schematic:

Enclosure - http://www.supertronic.com/en/cajas_de_plastico/sensors/29/pp42/50

Sensor module - https://www.aliexpress.com/item/GY-BME280-3-3-precision-altimeter-atmospheric-pressure-BME280-sensor-module/32688623437.html

ESP-01 - https://www.aliexpress.com/item/ESP8266-ESP-01S-ESP01S-Serial-Wireless-Module-Wifi-Sensor-ESP8266-ESP-01-Updated-for-Arduino-Wifi/32948119527.html

Power supply to the board can be provided in two ways:
 - via DC1
 - via JP1

DC1 is a 5.5x2.1mm barrel socket
JP1 is 2-pin 2.54mm spacing male header
 
Input voltage range is 5-40V as per the Datasheet of the regulator, although i haven't tested it with voltages higher than 12V. 
It can be easily powered by a simple USB-to-UART dongle for dev purposes.

Sensors which are compatible are essentially BME280,BMP280,BMP180,Si7021,SHT21,etc. which follow the pinout. I've tested it with BME280,BMP280,Si7021 - the modules which i have follow the same pinout and are working. Sensor support depends on the firmware of course.
