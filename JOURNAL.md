---
title: "Homeassistant automatic greeenhouse"
author: "Felix Wittwer (fegolix)"
description: "Automatic greenhouse with Homeassistant integration."
created_at: "2024-03-25"
---

# Journal

Here you can see a documentation of the entire development process.

**Total hours spent: 14h**

## 25th May (30m)

Just setting up the Git Repo. Finding some cool badges for the README.md file. Doing some parst reasearch.

![Home Assistant](https://img.shields.io/badge/home%20assistant-%2341BDF5.svg?style=for-the-badge&logo=home-assistant&logoColor=white)

![Static Badge](https://img.shields.io/badge/Hack_Club_HIGHWAY_TO_UNDERCITY-Hack_Club?style=flat&logo=hackclub&color=white)

## 29th May (1h)

Finding 3D Models for electrical box and other parts. It actually took some time to find a 3D model of the electrical Box I want to repurpose for the project. And because I am sometimes a lazy person [here its more about effectiveness; who needs to design a box when manufacturues profide the files :)] But from my experiente they like to hide them.

I eventually found the .stp files I was searching for and imported them into Fusion 360. Looks great and will defenitly better visualize the Idea and is perfect for planning.

<p float="left">
  <img src="./journal%20files/2025-05-29/electrical_box_fusion.png" height="400" />
  <img src="./journal%20files/2025-05-29/main_switch_fusion.png" height="400" />
</p>

## 30th May (7h 30m)

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

## 5th June (2h)

### Session 1 (1h 30m) during live call

I thought my project could need some proper branding and logo to let the README look nice. As my go to software for vectorgraphics I used Inkscape to do the logo. As my Project is compatible with Home Assistant I started with importing the Homeassistant logo. For my logo I wanted something that is simple and matches the astetic of Home Assistant.

<p float="left">
  <img src="./journal%20files/2025-06-05/Inkscape_design_logo.png" height="300" /> &nbsp; &nbsp;&nbsp;&nbsp;
  <img src="./journal%20files/2025-06-05/green-assistant-icon.svg" height="300" />
  <img src="./journal%20files/2025-06-05/green-assistant-logo-white.svg" height="300" />
</p>

### Session 2 (30m) during live call

I have added the Dallas temperature sensor module. Mostly it was code because the ground temperature sensors are already encapsulated. In my project two of those sensors will be used just for fun and because I have them laying arround. It defenitely will be interesting to see how the ground temperature is changing over the day.

## 23rd June (4h)

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