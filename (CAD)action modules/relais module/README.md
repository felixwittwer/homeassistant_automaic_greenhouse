# relais module

**Mandatory for irrigation system!**

| requires                                                            | mandatory for                 |
| ------------------------------------------------------------------- | ----------------------------- |
| none (control system aka ESP should be inplace but that is obvious) | irrigation system (solanoids) |

<br>

This folder contains everything regarding the hounting and implementation of the relais module.

Be aware that this module is only needed if you want to set up an irrigation system. It then will controll the individual solanoids.

Rough model of the Relais module:

![relais board](./relais%20board/relais_board.png)


I know every relais board will have mounting holes somewhere else so adjust it to your needs. To my knowledge the relais board I am using is no longer in production.

![relais board drawing](./relais%20board/relais_board_drawing.png)

## mounting / 3D printing

you will need to print mounting hardware for attatching the relais board to DIN rails. Besides the part irselt you need four M3 15mm screws and corrsponding nuts.

<img src="./images/Relais Module mounting.gif" height="400" />


## ESPHome config

This should be part of your ESPs yaml config file inside ESPHome.

``` yaml
#Relais
switch:
  - platform: gpio
    pin: GPIO16
    name: "Relay 1"
  - platform: gpio
    pin: GPIO17
    name: "Relay 2"
  - platform: gpio
    pin: GPIO18
    name: "Relay 3"
  - platform: gpio
    pin: GPIO19
    name: "Relay 4"
```