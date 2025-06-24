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

## The project

A list of all uesd parts can be found in the **parts** directory.

All files corresponding to the main part of the project so the electrical box with all the controll electronics can be found in the **core** directory.

{{ An explosion drawing of the electrical box will soon be here. }}

## Homeassistant Configuration and Dashboards

All stuff regarding Homeassistant can be found in the **homeassistant files** directory. Dashboards will be in a seperate folder.

<br>

# LICENSE
This work is licensed under CC BY-NC-SA 4.0. 

To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/4.0/

[![licensebuttons by-nc-sa](https://licensebuttons.net/l/by-nc-sa/3.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0)

