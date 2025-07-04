---
title: "Homeassistant automatic greeenhouse"
author: "Felix Wittwer (fegolix)"
description: "Automatic greenhouse with Homeassistant integration."
created_at: "2024-03-25"
---

# Journal

Here you can see a documentation of the entire development process.

**Total hours spent: 36h**

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

## June 24th (13h): Setting up Homeassistant

### Session 1 (3h)

I grabed my Raspberry Pi 4 B and an SD card and got right to installing Homeassistant for testing. In the future I will be running Homeassistant inside a VM on my NAS which is running TrueNAS Scale. While the image was downloading and later on installing on the Pi 4 I put togetehr a first prototybe with all the sensors I already have. I am going to use an ESP32 with ESPHome on it.

I directly connected the RPi4 to our Router via internet and noticed that it is actually supported by Homeassistant automaticaly and I can now monitor aour nethwork useage via Homeassistant, cool stuff :). Under Add-ons I have now installed the ESPHome Device Builder. Now I can begin building a full yaml config with all the snippets I already have inside the individual sensor module folders.  

<p float="left">
  <img src="./journal%20files/2025-06-24/RPi4.jpg" height="300" />
  <img src="./journal%20files/2025-06-24/first_prototype_with_the_parts_I_have.jpg" height="300" />
</p>

<img src="./journal%20files/2025-06-24/first_home_dashboard.png" height="300" />

### Session 2 (5h)

ESPHome is now setup and running with the sensors I currently have. To get it working I put together all the small snippets I already had written for each sensor module. The current setup consists of 4 soil moisture sensors, one DHT22, two DS18B20 soil temperature sensors and a realy board.

<p float="left">
  <img src="./journal%20files/2025-06-24/esphome_log.png" height="300" />
  <img src="./journal%20files/2025-06-24/epshome_yaml.png" height="300" />
</p>

After a lot of tinkering I got a cool dasboard together and it is working! especially styling and placing the sensor values on the map was difficult. It now correctly displays the values of the sensors I have currently set up. Because I have multiple zones for the irrigration and sensors I decided to use Homeassistants stack and map components. A notmal stack of components wouldn't be so resonsive (I want to us it on mobile and desktop and later on maybe on a dashboard) I decided to split things up in collumns and addes some stacks in beetreen that can be easialy resized by the device on the corresponding platform. I kind of fell in love with the dashboard maps and created a floor plan of our greenhouse to get a better Idea where the sensors are located in real life. There is now a map for genreal environment sensors, soil moisture sensors, irrigation system and ground temperature sensors. As a small additon I added small badges at the top of the page to have the irrigation system easialy accesible.

<img src="./journal%20files/2025-06-24/homeassistant_dashboard.png" height="300" />

### Session 3 (4h): main PCB design

Since my prototype cabeling is an absolute mess and everything should be organized inside the electrical box I designed a shield pcb for the ESP32 S3 I am using. I acutally only need the PCB without assembly because I have most of the parts and from my experience JLC PCB most times does not have screw in terminals with a 5mm pin distance. Furthermore assemby is unresonably expensive for some parts that aren't smd. I intentionally designed the resistors to be non smd so they can be switched if needed. I don't know maybe the very humid enviroment isn't the best even if mostly sealed inside a the electrical box. Additionally I don't know weatcher I need the other pins of the ESP32 in the future so I decided on giving them some headers.

<img src="./journal%20files/2025-06-24/pcb_preview.png" height="300" />

<br>

<p float="left">
  <img src="./journal%20files/2025-06-24/pcb_preview copy.png" height="350" />
  <img src="./journal%20files/2025-06-24/pcb_shield_schematics.png" height="350" />
</p>

### Session 4 (1h): PCB mount deisgn

Becaus the PCB will defenitely wont float and will need some mounting hardware I did just that. If you are wondering how I pulled taht of especially with the random hole design of my PCB (I havent bothered to make something with nice measurements and just placed them here no traces were), I exported the PCB in KiCad to a wrl file and opened that with Blender inside Blender I exported it to an stl file (makre sure to chosse scale 1000 or else your pcb will just be a fractions of milimeters long) and importet this into Fusion 360 where I traced the holes from the stl model.

<img src="./journal%20files/2025-06-24/pcb_mount.png" height="300" />

## June 25th (4h): adding irrigation system and finishing of

### Session 1 (1h): mounting for relais board

My costom PCB already had a mount but to make it perfect also the relay board needed some mounting hardware. In the end I decided to attatch the PCB via 15mm long M3 screws and correspondign nuts.

<img src="./journal files/2025-06-25/relais_mounting.png" height="400" />

### Session 2 (1h): planning for irrigation tubing

Since all electronic parts are done now we have to think of a way to water your beloved plants inside the greenhouse. I decided to go with a 4 in 1 solanid that is perfect for my 4 zone watering system. Between all the components 10 mm PVC tubing will be used. All the individual parts for connecting the individual tube pieces will be 3D printed. So for each plant you need a t piece and a nozzle to water it. I will maybee adjust the nozzle size in the future but for now it should work. Anothe Idea might be to make kind of an l piece at the end to save on the end piece but then the entife l piece nedds to be redesigned and not just the nozzle.

<p float="left">
  <img src="./journal files/2025-06-25/solanoids.jpg" height="300" />
  <img src="./journal files/2025-06-25/tubing_map.png" height="300" />
</p>

<p float="left">
  <img src="./journal files/2025-06-25/t-piece.png" height="200" />
  <img src="./journal files/2025-06-25/end-piece.png" height="200" />
  <img src="./journal files/2025-06-25/nozzle-piece.png" height="200" />
</p>

### Session 3 (2h): adding a wiring diagramm

Most wiring is done with the PCB but all the sensor still need to be connected. Here comes the electrical box into play. I am going to use the old already in place DIN rails to mount everything from the relais to the custom PCB inisde. All the sensors will be outside of the box in the places where they need to be. Besides the wiring diagram I finisted the design of the electrical box and arranged its components.

<img src="./journal files/2025-06-25/wiring diagram.png" height="400" />
<img src="./journal files/2025-06-25/core_electrical_box.png" height="400" />

### Session 4 (1h): writing some documentation and making it easier to create your custom Green Assistant

Because it could be difficult to understand the projects structure I designed a small diagram on where to start and how to configure your Green Assistant. With this map someone else could easealy start building theor own smart greenhouse. Besides that I extended the main README file a bit.

<img src="./journal files/2025-06-25/your_green_assistant.png" height="500" />

## June 30th (2h)

### Session 1 (2h): researching parts and creating BOM

As one of the last steps of the planing phase I finished the BOM list of the project luckily I have most parts of my BOM already at home and also can 3D print parts at home. Fort somebody that is going to build his own system it is imortant to nate that you defenitely don't need a industrial grade waterproof electrical box but we already had one so why don't use it. But for anyone else: you will be fine with buying a DIN Rail and mounting your stuff to it.

### Session 2 (2h): doing some final touchups and completing ESPHome config

I have noticed that I have forgotten to add some codesnippets form the individual sensors to the main ESPHome config so I did that now. I have designed and coded all parts for the window and door sensors but forgot them on the PCB. This isn't bad at all because I thought about having all remaining pins pined out so I can add some stuff later on. The PCB has the perfect formfactor and I will not change it now because of space inside the electrical box. The sensors can still be added easily.