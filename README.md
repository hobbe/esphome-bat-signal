# Bat-Signal Light Controller

## Material

- Wemos D1 mini
- RGD 12-bit LED ring (WS2812)

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
