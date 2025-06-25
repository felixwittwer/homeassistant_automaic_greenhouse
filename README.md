![Home Assistant](https://img.shields.io/badge/home%20assistant-%2341BDF5.svg?style=for-the-badge&logo=home-assistant&logoColor=white) &nbsp; &nbsp; ![ESPHome_Badge](https://img.shields.io/badge/ESPHome-ESPHome?style=flat&logo=esphome&labelColor=212121&color=212121)

![Static Badge](https://img.shields.io/badge/Hack_Club_HIGHWAY_TO_UNDERCITY-Hack_Club?style=flat&logo=hackclub&color=white)

<br>
<p align="center">
    <img src="branding/green-assistant-logo-white.svg" style="width: 80%">
</p>
<br>

# homeassistant_automaic_greenhouse
A cool Project to make your greenhouse smart. What about automaic irrigation and collecting enviromental data right from your garden.

## About the project
This project actually is sthe second iteration on me trying to automate our greenhouse. The first version relied on an Arduino Uno powered by a 24V powertool battery and sensordata was logged to an SD-card. Since we now have power and wifi connectivity to the greenhouse I wanted to step up the game and build something that is way smarter and will hopefully last forever. If you were wondering this is why an industrial grade electrical box with rails was used.

## The concept of sensor and action modules
This project is a very speced out version of a greenhouse automation and environmental monitoring system. Due to cost or other reasons you might not include all the sensors used by me. To make it easyer to do so each sensor is getting his own folder inside the sensor modules directory. You will find everything you need to know about a so called sensor module inside this folder from CAD files, STL Files for 3D printing and scematics to instructions on sourcing the parts.

A detailed list of all sensors used in the project can be found in the **sensor modules** directory.

Like the sensors you might choose to leave out some action modules aka the parts that actually do something like the relais and solanoids for an irrigation system.

These so called action modules with all their corresponding documentation and files can be found in the **action modules** directory.

## Where to start

If you are completly new to this project you might take a look at the folowing map. Go thrugh the individual questions and build your own Green Assistant. Follow the link below to get to an interactive pdf version. Clicking on the links will be more func than searching in this Repo.

<img src="./your_green_assistant.png" height="400" />

![Interactive PDF version](./your_green_assistant.pdf)

## The project

A list of all uesd parts can be found in the **parts** directory.

All files corresponding to the main part of the project so the electrical box with all the controll electronics can be found in the **core** directory.

<img src="./core/electrical box/core_electrical_box.png" height="400" />
<img src="./core/electrical box/Eaton_Box_ci44x_125_na v20.gif" height="400" />

### PCB

You will need this PCB to connect all sensors reliably to the ESP32 S3. All unused pins of the ESP also have a connection to a pinheader so you are free to add sensors without needing to modify the PCB. 

PCB Sourcefiles can be found inside [core/esp32 pcb and mounting/pcb files/esp shield](./core/esp32%20pcb%20and%20mounting/pcb%20files/esp_shield/).

<img src="./core/esp32 pcb and mounting/pcb files/pcb_preview copy.png" height="400" />

<p float="left">
  <img src="./core/esp32 pcb and mounting/pcb files/pcb_preview.png" height="350" />
  <img src="./core/esp32 pcb and mounting/pcb files/pcb_shield_schematics.png" height="350" />
</p>

### Wiring

Wehn you have coosen your parts and want to build your Green Assistant have alook at this wiring diagramm of all the sensors.

<img src="./core/wiring diagram.png" height="400" />

### Homeassistant Configuration and Dashboards

All stuff regarding Homeassistant can be found in the **homeassistant files** directory. Dashboards will be in a seperate folder.

<img src="./homeassistant files/images/homeassistant_dashboard.png" height="400" />

<br>

# LICENSE
This work is licensed under CC BY-NC-SA 4.0. 

To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/4.0/

[![licensebuttons by-nc-sa](https://licensebuttons.net/l/by-nc-sa/3.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0)

