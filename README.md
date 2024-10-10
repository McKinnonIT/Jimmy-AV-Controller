ESPHome Jimmy CYD Touch Display for Projector Control
======
### Overview
This project utilizes a JC2432W328 capacitive touch ESP32 board to control a projector through a custom touch interface built using ESPHome. The control board features an integrated ILI9341 display with touch support, and it allows users to power the projector on or off, switch inputs and adjust the volume via UART connection. The UART commands provided are for Epson projectors but they can easily be modified to accommodate different projector models as needed. 
### Hardware:
 - ESP32-JC2432W328
 - RS-232 to TTL UART Module
 - RJ45 Screw Terminal adapters x2
 - DC 5v 1A power adapter

### Installation

We chose to use the existing Ethernet cables running from the projector to the control board's mounting location, utilizing RJ45 screw terminals at both ends for convenience. However, alternative cabling options are possible. The key requirement is to provide 5V power, ground, TX and RX to both RS232 TTL and the board. We wired the power adapter to the same pins as the RS232 TTL and connected the TX and RX terminals to the corresponding GPIO pins on the board. This setup delivers power to the ESP32 while allowing it to send UART commands to the RS232 TTL, which is connected to the projector.





We also designed a custom 3D-printed holder to allow the control board to be wall-mounted, ensuring it fits perfectly within standard AU wall plate spacing either with a J bracket or using a surface mounting box.


