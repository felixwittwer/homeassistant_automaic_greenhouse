# DS18B20 sensor module

The DS18B20 is used for measuring ground temperature. Just for fun this project uses two sensors because they came in a pack of two you will be fine with one.

| part name       | amount     | price          |   | things you need |
| --------------- | ---------- | -------------- | - |---------------- |
| DS18B20 2 meter cable | 1          | ~1.17 USD      | https://de.aliexpress.com/item/1005008024174225.html?spm=a2g0o.productlist.main.2.892a1a0e74KpG7&algo_pvid=fdca3388-9d61-4050-a1fa-ad9c645db0ba&pdp_ext_f=%7B%22order%22%3A%221023%22%2C%22eval%22%3A%221%22%7D&utparam-url=scene%3Asearch%7Cquery_from%3A  | ---             |
| some wire       | 1          | ~              |   | ---             |

## ESPHome config

``` yaml
sensor:
  - platform: dallas_temp
    address: 0x1234567891234567
    name: temperature_ds18b20_1
    update_interval: 60s
  - platform: dallas_temp
    address: 0x1234567891234567
    name: temperature_ds18b20_2
    update_interval: 60s
```

The adresses are just placeholders and need to be replaced by the actual sensor adresses.

Upload the following code to your ESP via ESPHome and watth the console log.

``` yaml
one_wire:
  - platform: gpio
    pin: GPIO25
```

Something like this should be returned. Replace the adresses in the configuration files with the ones returned by the console. 

<!-- c was used for code here because formating looks nice -->
``` c
[02:53:52][C][gpio.one_wire:020]: GPIO 1-wire bus:
[02:53:52][C][gpio.one_wire:021]:   Pin: GPIO25
[02:53:52][C][gpio.one_wire:080]:   Found devices:
[02:53:52][C][gpio.one_wire:082]:     0xee00000083a76028 (DS18B20)
[02:53:52][C][gpio.one_wire:082]:     0x43000000854b5628 (DS18B20)
```