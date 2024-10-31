ESPHome Jimmy CYD Touch Display for Projector Control
======
### Overview
This project utilizes a JC2432W328 capacitive touch or 2432S028R resistive touch ESP32 board to control a projector through a custom touch interface built using ESPHome. The control board features an integrated ILI9341 display with touch support, and it allows users to power the projector on or off, switch inputs and adjust the volume via UART connection. The UART commands provided are for Epson projectors but they can easily be modified to accommodate different projector models as needed. 
### Components:
 - [ESP32-JC2432W328](https://vi.aliexpress.com/item/1005006948064622.html) or [ESP32-2432S028R](https://vi.aliexpress.com/item/1005007095061705.html)
 - [RS-232 to TTL UART Module](https://vi.aliexpress.com/item/1005006807931160.html)
 - [RJ45 Screw Terminal adapters x2](https://vi.aliexpress.com/item/1005006037699995.html)
 - [Female DC 5.5 2.1mm terminal adapter](https://vi.aliexpress.com/item/1005006755773620.html)
 - [DC 5v 1A power adapter](https://vi.aliexpress.com/item/32722341492.html)
 - [JST PH 4-Pin to Male Header Cable - I2C STEMMA Cable](https://core-electronics.com.au/jst-ph-4-pin-to-male-header-cable-i2c-stemma-cable-200mm.html)
 - [1m DB9 RS232 Serial Null Modem Cable F/F](https://www.mwave.com.au/product/startech-1m-black-db9-rs232-serial-null-modem-cable-ff-ab86700)
 - Electrical Wire 20AWG
 - 20AWG Ferrules x10
 - 3D Printed Wallplate and Cover
 - 3D Printed Breakout Box


### Installation
#### Step 1
- Flash the ESP32 touch board with relevent code and ensure buttons are displayed and react to user input
##### Step 2 
- Connect JST cable to RJ45 terminal block
#### Step 3
- Wire the Female DC, RS232 and R45 terminal block and secure in breakout box
#### Step 4
- Install wallplate and ESP32 board in desired location and connect RJ45 cable
#### Step 5
- Place breakout box in desired location and connect power, DB9 cable to projector and RJ45 cable
#### Step 6
- Installation is now done, test the projector is responding to commands sent from the ESP32 board

