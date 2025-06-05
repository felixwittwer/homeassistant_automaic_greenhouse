# DS18B20 sensor module

The DS18B20 is used for measuring ground temperature. Just for fun this project uses two sensors because they came in a pack of two you will be fine with one.

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