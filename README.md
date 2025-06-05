# Jimmy AV Controller

## 🧩 Project Overview  
The Jimmy AV Controller is an open, customizable solution for projector and AV control over RS232. It is designed to address the limitations of existing commercial systems—closed ecosystems, high costs, poor interfaces, and no easy way to monitor usage and automate groups of projectors & TVs.

It’s designed for use in classrooms, conference rooms, and anywhere you want RS232 control over AV equipment.  
With touchscreen ESP32 boards like the JC2432W328 (capacitive) and 2432S028R (resistive), which support native LVGL in ESPHome, we built a customizable, user-friendly control panel that integrates easily with ESPHome and Home Assistant.  
We chose ESPHome for its popularity and maintainability, with many examples and community support already available.

<p align="center">
  <img src="https://github.com/McKinnonIT/Jimmy-AV-Controller/blob/main/OnScreen.jpg?raw=true" width="29%" />
  <img src="https://github.com/McKinnonIT/Jimmy-AV-Controller/blob/main/OffScreen.jpg?raw=true" width="29%" />
</p>

## 🧠 How it works

The Jimmy AV Control System uses an ESP32 touchscreen panel to send RS232 commands to AV gear, integrating seamlessly with ESPHome and Home Assistant for easy automation and monitoring.

At its core, the system includes:
- ESP32 touchscreen (capacitive JC2432W328 or resistive 2432S028R) flashed with ESPHome
- LVGL customisable GUI
- 3D-printed wall plate & breakout box for secure mounting  
- RS232 to TTL UART breakout box  
- RJ45 Ethernet cables to connect breakout box to wall plate touchscreen  
- Generic DC power supply  

Using the ESPHome Web Flasher makes setup simple.

![System Diagram](https://github.com/McKinnonIT/Jimmy-AV-Controller/blob/main/JimmyAVDiagram.png)

## ⚙️ Parts
- ESP32-JC2432W328 or ESP32-2432S028R (CYD)
- RS-232 to TTL UART Module
- RJ45 Screw Terminal adapters x2
- Female DC 5.5 2.1mm terminal adapter
- DC 5v 2A power adapter
- Electrical Wire 20AWG
- 20 AWG Ferrules
- M2.5 10mm Screws
- RJ45 cable (run from wall plate location to projector)
- 3D Printed Wall Plate and Cover
- 3D Printed Breakout Box

## 🛠️ Installation

1. Wire JST cable to RJ45 terminal and plug into the flashed touchscreen  
2. Wire the female DC terminal adapter, RS232 TTL module, and RJ45 terminal block; secure inside the breakout box  
3. Mount the 3D-printed wall plate, connect Ethernet, screw in touchscreen, and snap on the wall plate cover  
4. Place the breakout box in a secure spot, connect the DB9 to projector, plug in Ethernet and power  

## 💾 Flashing Touchscreen

### 🔌 Using ESPHome

Make sure `capacitive.yaml`, `resistive.yaml`, `lvgl.yaml`, and `epsonswitch.yaml` are in the `esphome/common` directory.

1. Connect the touchscreen via USB-C  
2. In ESPHome, create a new device, name it, and select the USB serial port  
3. Modify the config to include secrets and relevant YAML files:

```yaml
    esphome:  
      name:  
      friendly_name:  

    esp32:  
      board: esp32dev  
      framework:  
        type: arduino  

    logger:  
      level: NONE  

    api:  
      encryption:  
        key: ""  

    ota:  
      - platform: esphome  
        password: !secret otapassword  

    wifi:  
      ssid: !secret wifi_ssid  
      password: !secret wifi_password  

    <<: !include common/capacitive.yaml  
    <<: !include common/lvgl.yaml  
    <<: !include common/epsonswitch.yaml  
```
4. Flash this config to the touchscreen. The display should now be interactive.

### 🌐 Standalone using ESPHome Web

Use this if Wi-Fi or Home Assistant isn’t needed.

1. Visit https://web.esphome.io  
2. Connect USB and click **Connect**  
3. Click **Install** and flash `jimmy-av-controller.factory.bin` or a custom `.bin`  

## 🖨️ 3D Printed Parts

This project includes custom 3D-printed enclosures to provide a clean and secure installation:

### 🧱 Included `.stl` Files:
- `lcd-wallplate.stl` – Main mounting frame for the ESP32 touchscreen  
- `lcd-wallplate-cover.stl` – Snap-on faceplate cover for a polished finish  
- `breakout-box.stl` – Compact enclosure for RS232, DC, and RJ45 connectors  

### ⚙️ Printing Notes:
- Standard **PLA settings** were used  
- The **breakout box** may require **supports**, depending on your printer and orientation  
- Successfully printed on:
  - **Creality K1C**
  - **Bambu Lab P1S**

> Parts were designed for ease of assembly and professional installation appearance.
