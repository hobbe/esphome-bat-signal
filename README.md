# Bat-Signal Light Controller

## Material

- Wemos D1 mini
- RGD LED

## Software

- ESPHome
- Home Assistant (optional)

## Setup

```yaml
substitutions:
  name: bat-signal
  friendly_name: Bat-Signal
  red_led_pin: D6
  red_led_power: 100%
  green_led_pin: D7
  green_led_power: 50%
  blue_led_pin: D8
  blue_led_power: 80%
packages:
  hobbe.bat-signal: github://hobbe/esphome-bat-signal/bat-signal.yaml@main
esphome:
  name: ${name}
  name_add_mac_suffix: false
  friendly_name: ${friendly_name}
api:
  encryption:
    key: !secret api_key
wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password
```
