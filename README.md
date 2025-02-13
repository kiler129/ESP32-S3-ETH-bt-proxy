# ESP-S3-ETH ESPHome Bluetooth Proxy


### Repository Contents
This repository contains configuration files used to build a firmware to create [Bluetooth/BLE proxy](https://esphome.io/components/bluetooth_proxy.html) 
usable with HomeAssistant using ESPHome. This repository targets [Waveshare ESP-S3-ETH](https://www.waveshare.com/esp32-s3-eth.htm), that is relatively cheap and available, while containing ethernet & PoE options. For other boards see [ESPHome's official repository](https://github.com/esphome/bluetooth-proxies).

### How to use it?
In general, see [official guide](https://esphome.io/guides/faq#how-do-i-install-esphome-onto-my-device), but the 
easiest/opinionated-best way to build it would be:

1. Get [`esphome` CLI toolkit](https://esphome.io/guides/getting_started_command_line.html) using your package manager 
   (e.g. using [`brew` on macOS](https://esphome.io/guides/installing_esphome#mac))
2. Copy `secrets.example.yaml` to `secrets.yaml` and fill-in the details
3. Connect the board using USB
3. Build & upload the firmware using
    - If you're using CLI tools simply do `esphome run bt-proxy.yaml`
    - If you want to change name you can do `esphome -s name my-cool-proxy -s long_name 'Cool BT Proxy' run bt-proxy.yaml`
4. Go and add it to HomeAssistant; once it's added BT devices will appear *automagically*
5. If you're not planning to rebuild this project multiple times, now it's time to `rm -rf ./.esphome` as it takes a lot
   of space after build
