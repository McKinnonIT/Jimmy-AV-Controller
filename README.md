Jimmy AV Controller
======
### Project Overview
The Jimmy AV Controller is an open, customizable solution for projector and AV control over RS232. It is designed to address the limitations of existing commercial systems—closed ecosystems, high costs, poor interfaces, and no easy way to monitor usage and automate groups of projectors & TV’s.

It’s designed for use in classrooms, conference rooms and anywhere you want RS232 control over AV equipment.
With the availability of touchscreen ESP32 boards like the JC2432W328 (capacitive) and 2432S028R (resistive) with native LVGL support in ESPHome, we developed a fully customizable, user-friendly control panel that integrates with ESPHome and Home Assistant for streamlined projector management. We built on ESPHome due to its wide adoption and easy to maintain with so many examples and projects already online.

### How it works:
The Jimmy AV Control System uses an ESP32 touchscreen panel to send RS232 commands to projectors and AV equipment, integrating seamlessly with ESPHome and Home Assistant for easy automation and monitoring.

At its core, the system consists of:

- ESP32 touchscreen (capacitive or resistive) flashed with ESPHome
- 3D-printed wall plate & breakout box for secure mounting
- RS232 to TTL UART breakout box to communicate with projectors / TV’s
- RJ45 Ethernet cables to connect breakout box to wall plate touchscreen
- Generic Power supply

By using ESPHome web flasher, setup and configuration of the Jimmy is very simple. 

