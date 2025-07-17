# MH-Z19B sensor module

| part name       | amount     | price          |   | things you need |
| --------------- | ---------- | -------------- | - |---------------- |
| MH-Z19B | 1          | ~21.68 USD      | https://de.aliexpress.com/item/4001296615950.html?spm=a2g0o.productlist.main.1.10df56e9kDzAiu&algo_pvid=496ed4bc-a93e-4799-9a9a-8ecbef09edf5&pdp_ext_f=%7B%22order%22%3A%2296%22%2C%22eval%22%3A%221%22%7D&utparam-url=scene%3Asearch%7Cquery_from%3A  | ---             |
| M3 screws 15mm  | 2          | ~              |   | ---             |
| M3 nuts         | 2          | ~              |   | ---             |
| some wire       | 1          | ~              |   | ---             |
| case top        | 1          | ---            |   | 3D printer      |
| case bottom     | 1          | ---            |   | 3D printer      |

[for screws and nuts have a visit you local hardware store or buy them in a larger pack]

The MH-Z19B will be used for CO2 measurements. I already have a lot of sensors lying arround and wanted something special that will be very interisting to analyse. Because we all know why plants need CO2. Maybee also the different kinds of photosnthesis can be monitored. All in all a cool sensor even though it is not the cheapes but also won't break the bank.

<img src="./images/MH-Z19B mount.gif" height="400" />

## housing

You will need both parts of the case and two M3 15mm long screws with nuts compatible with your greenhouses aluminium extrusions. 

## 3D printing

The desing works totally fine with my SLA printer and Anycubig tough resin. You might need to think about placing your supports and material choices. The tough resin I use is a bit elastik so the clips dont snap of and can be bend temporarily during assembly.

STL Files are inside this folder.

## ESPHome config

``` yaml
sensor:
  - platform: mhz19
    co2:
      name: MH-Z19 CO2 Value
    temperature:
      name: MH-Z19 Temperature
```

this sensor communicates ofer UART so a uart config is mandatory

``` yaml
uart:
  tx_pin: GPIOXX
  rx_pin: GPIOXX
  baud_rate: 9600
```