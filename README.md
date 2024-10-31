ESPHome Jimmy CYD Touch Display for Projector Control
======
### Overview
This project utilizes a JC2432W328 capacitive touch ESP32 board to control a projector through a custom touch interface built using ESPHome. The control board features an integrated ILI9341 display with touch support, and it allows users to power the projector on or off, switch inputs and adjust the volume via UART connection. The UART commands provided are for Epson projectors but they can easily be modified to accommodate different projector models as needed. 
### Components:
 - [ESP32-JC2432W328](https://vi.aliexpress.com/item/1005006948064622.html) or [ESP32-2432S028R](https://vi.aliexpress.com/item/1005007095061705.html)
 - [RS-232 to TTL UART Module](https://vi.aliexpress.com/item/1005006807931160.html)
 - [RJ45 Screw Terminal adapters x2](https://vi.aliexpress.com/item/1005006037699995.html)
 - [Female DC 5.5 2.1mm terminal adapter](https://vi.aliexpress.com/item/1005006755773620.html)
 - [DC 5v 1A power adapter](https://vi.aliexpress.com/item/32722341492.html)
 - [JST PH 4-Pin to Male Header Cable - I2C STEMMA Cable](https://core-electronics.com.au/jst-ph-4-pin-to-male-header-cable-i2c-stemma-cable-200mm.html)
 - Wire

### Installation

We chose to use the existing Ethernet cables running from the projector to the control board's mounting location, utilizing RJ45 screw terminals at both ends for convenience. However, alternative cabling options are possible. The key requirement is to provide 5V power, ground, TX and RX to both RS232 TTL and the board. 
At the wallplate end we connect the JST 4-Pin to the board and connect the headers to the RJ Terminal adapter, at the projector end we use the jumper wires to connect the RS232 module to the correct GND, 5v, TX and RX pins as well as splicing in 5v and Gnd from the power adapter (we used an old chromecast power adapter). This setup delivers power to the ESP32 while allowing it to send UART commands to the RS232 TTL, which is connected to the projector.





We also designed a custom 3D-printed holder to allow the control board to be wall-mounted, ensuring it fits perfectly within standard AU wall plate spacing either with a J bracket or using a surface mounting box.


