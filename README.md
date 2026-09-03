# Flexispot E7Q ESPHome

ESPHome configuration for a Seeed Studio XIAO ESP32-C6 connected to a Flexispot
E7Q desk. It combines the XIAO ESP32-C6 pinout guidance from
[dimitri-vs/flexispot-esphome](https://github.com/dimitri-vs/flexispot-esphome)
with the `loctekmotion_desk_height` external component from
[iMicknl/LoctekMotion_IoT](https://github.com/iMicknl/LoctekMotion_IoT).

Use `desk.yaml` as the ESPHome configuration. Before compiling, set these
values in ESPHome's `secrets.yaml`:

```yaml
wifi_ssid: "your Wi-Fi SSID"
wifi_password: "your Wi-Fi password"
api_encryption_key: "your ESPHome API encryption key"
fallback_hotspot_password: "a fallback hotspot password"
```

The default pin mapping is GPIO16 (D6) for desk commands, GPIO17 (D7) for
height data, and GPIO2 (D2) for the screen wake signal. Adjust the
substitutions in `desk.yaml` for a different desk height range or unit.