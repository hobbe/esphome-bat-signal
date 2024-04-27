# Bat-Signal Light Controller

## Material

- Wemos D1 mini
- RGD 12-bit LED ring (WS2812)

![image](https://github.com/hobbe/esphome-bat-signal/assets/312886/c827ad01-4de0-404a-b293-b7c092382539)

|D1 mini|WS2812|
|---|---|
|G|GND|
|5V or 3V3|5V|
|GPIO03 / RX|Din|

## Software

- ESPHome
- Home Assistant (optional)

## Setup

```yaml
substitutions:
  name: bat-signal
  friendly_name: Bat-Signal
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
