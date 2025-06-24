---
title: "Homeassistant automatic greeenhouse"
author: "Felix Wittwer (fegolix)"
description: "Automatic greenhouse with Homeassistant integration."
created_at: "2024-03-25"
---

# Journal

Here you can see a documentation of the entire development process.

**Total hours spent: 16h**

## May 25th (30m): initial setup

Just setting up the Git Repo. Finding some cool badges for the README.md file. Doing some parst reasearch.

![Home Assistant](https://img.shields.io/badge/home%20assistant-%2341BDF5.svg?style=for-the-badge&logo=home-assistant&logoColor=white)

![Static Badge](https://img.shields.io/badge/Hack_Club_HIGHWAY_TO_UNDERCITY-Hack_Club?style=flat&logo=hackclub&color=white)

## May 29th (1h): start desingning core electrical box

Finding 3D Models for electrical box and other parts. It actually took some time to find a 3D model of the electrical Box I want to repurpose for the project. And because I am sometimes a lazy person [here its more about effectiveness; who needs to design a box when manufacturues profide the files :)] But from my experiente they like to hide them.

I eventually found the .stp files I was searching for and imported them into Fusion 360. Looks great and will defenitly better visualize the Idea and is perfect for planning.

<p float="left">
  <img src="./journal%20files/2025-05-29/electrical_box_fusion.png" height="400" />
  <img src="./journal%20files/2025-05-29/main_switch_fusion.png" height="400" />
</p>

## May 30th (7h 30m): configuring my electrical box

### Session 1 (1h 30m)

I just wrote some imortant stuff to the README and build a logical project structure. The README also explains the concept of sensor modules. The concept of sensor moduels I introduced makes it easy to adapt and adjust the project to you individual needs. I added a License fole just to be clear on how the project can be used in the future.

### Session 2 (2h 30m)

I modeled some parts on my own like the ground plate on the inside of the box where everything is mounted. Furthermore I added the main switch and DIN Rais inside the box with some terminals for the wires. I also decided on writing sub README files for the individual folders bacause Github can't display lager 3D files. Now there will be great renders right in every directory. 

<p float="left">
  <img src="./journal%20files/2025-05-30/electrical_box_fusion.png" height="300" />
  <img src="./journal%20files/2025-05-30/core_electrical_box.png" height="300" />
</p>

### Session 3 (2h 30m)

For the first sensor modul to design I decieded on the window contacts which are based on reed switches and magnets. These sensors will be designed for our greenhouse and the aluminium extrusions it uses. To attatch my 3D printed parts to the aluminium extrusions I thought of M3 screws and corresponding nuts. The case fo the reed sensor and magnet are designed in such a way that ti is possible to assemble the housing without screws just with the clips on the sides. 

<p float="left">
  <img src="./journal%20files/2025-05-30/window_contact_sensor_module.png" height="300" />
  <img src="./journal%20files/2025-05-30/greenhouse_window.jpg" height="300" />
</p>

### Session 4 (1h)

I am going to desing cases for all components so they can be mounted on the existing DIN rails. But to build a case around my parts I first need them to be in CAD. Because my relais module is out of production and the screwholes are custom for almost every board out there I quicly sketched up mine. Besides I modeled the bottom terminal row completly like it is right now in real life. Additionally I added a 5V and 9V rail mounted powersupply. The 5V one is for the ESP and relais board while the 9V one is for supplying the solanoids with power. The solanoids will be controlled by the relais board.

<p float="left">
  <img src="./journal%20files/2025-05-30/relais_board.png" height="300" />
  <img src="./journal%20files/2025-05-30/core_electrical_box_2.png" height="300" />
</p>

## June 5th (2h): add some branding and Dallas sensor module

### Session 1 (1h 30m) during live call

I thought my project could need some proper branding and logo to let the README look nice. As my go to software for vectorgraphics I used Inkscape to do the logo. As my Project is compatible with Home Assistant I started with importing the Homeassistant logo. For my logo I wanted something that is simple and matches the astetic of Home Assistant.

<p float="left">
  <img src="./journal%20files/2025-06-05/Inkscape_design_logo.png" height="300" /> &nbsp; &nbsp;&nbsp;&nbsp;
  <img src="./journal%20files/2025-06-05/green-assistant-icon.svg" height="300" />
  <img src="./journal%20files/2025-06-05/green-assistant-logo-white.svg" height="300" />
</p>

### Session 2 (30m) during live call

I have added the Dallas temperature sensor module. Mostly it was code because the ground temperature sensors are already encapsulated. In my project two of those sensors will be used just for fun and because I have them laying arround. It defenitely will be interesting to see how the ground temperature is changing over the day.

## June 23rd (6h): desinging sensor modules

### Session 1 (2h)

After creating a cool loking logo and branding I decided to go on with designening the sensor and action modules. The next one in line was the light sensor module. Measuring light intensity might be really interesting to see in a greenhouse environment.

<img src="./journal%20files/2025-06-23/lux_sensor_case.png" height="300" />

I also decided on using a new standardised format for each sensor and action module. Each of them has it's own Readme with a seperate BOM this should improve the experience for users who want to build a simialr project but don't need as many sensors.

### Session 2 (1h)

I have updated some sensor moduel READMEs now to accomidate the new format. Additionally I finished the homeassistant configuration for the window and door contacts. Some inforamtions form the window contacts module regarding 3D printing instructions was also copied.

Up until now I think the README for the window contacts is my favourit with its animated gif ot the CAD model and the BOM with parts at the top.

### small break

visiting the greenhouse and touching some grass outside :) aka not beeing glued to my monitor

### Session 3 (1h)

New sensor module! I have most of the parst already at home so Hackclub doesn't need to pay for them. One sensor that will be particularly interesting for greenhouse monitoring is a CO2 sensor which I unfortunately don't have. So now it's the time to add it to the project. It is is bit more expensive thatn a DHT22 or other sensor but with about 20$ also won't break the bank. Designing a mounting system was a bit difficult because I had nothign to measure of but I eventually found a datasheet with dimensions on it. In the end I decided to design a simple clamp over the sensor that can be mounted to the aluminium extrusions with two M3 screws and fitting nuts.

<img src="./journal%20files/2025-06-23/mh-Z19B_mount.png" height="300" />

### Session 4 (1h)

One of the last sensor modules. Yeah! I have soldered some wires on the DHT22 sensor I had in my drawer. Forunately The sensor as a 3mm hole at the top so a M3 screw fits perfectly and I don't need to desing a custom mounting solution. I thought about adding a 3D printed shield for the sensor to protect it against direct sunlight. Currentyl it will be mounted behind the aluminium extrusion of the greenhouse so direct sunlight hopefully won't be an issue.

<img src="./journal%20files/2025-06-23/DHT22.jpg" height="300" />

### Session 5 (1h)

For now the last sensor module is complete. Prpbably the most important one for a greenhouse automation, the soil moisture sensors. i decided to go with capaciative ones pecause they dont degrade or not as easealy as some others with metal rods. Additionally I had themy lying around so why not use them :). The Homeassistant configuration I build also contains the calibration logic that has to be used once to tell the sensor what is dry and what is wet. Somebody rebuilding my procet can therefore easily build a similar setup.

<img src="./journal%20files/2025-06-23/capaciative_soil_moisture_sensor.JPG" height="300" />

## June 24th (3h): Setting up Homeassistant

### Session 1 (3h)

I grabed my Raspberry Pi 4 B and an SD card and got right to installing Homeassistant for testing. In the future I will be running Homeassistant inside a VM on my NAS which is running TrueNAS Scale. While the image was downloading and later on installing on the Pi 4 I put togetehr a first prototybe with all the sensors I already have. I am going to use an ESP32 with ESPHome on it.

I directly connected the RPi4 to our Router via internet and noticed that it is actually supported by Homeassistant automaticaly and I can now monitor aour nethwork useage via Homeassistant, cool stuff :). Under Add-ons I have now installed the ESPHome Device Builder. Now I can begin building a full yaml config with all the snippets I already have inside the individual sensor module folders.  

<p float="left">
  <img src="./journal%20files/2025-06-24/RPi4.jpg" height="300" />
  <img src="./journal%20files/2025-06-24/first_prototype_with_the_parts_I_have.jpg" height="300" />
</p>

<img src="./journal%20files/2025-06-24/first_home_dashboard.png" height="300" />