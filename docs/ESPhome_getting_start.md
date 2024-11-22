# Getting started with the ESPHome version

Our boards from tynet.eu ship with the normal Arduino based Firmware that is simple to use out of the box.
Sadly this software that was developed over the past years got some minor inconveniences that are not simple to fix.
If you are one of the few people that have an issue with th software or just wan't to use ESPHome instead you can follow this guide

ESPHome uses a native Home Assistant API instead of MQTT and is simple to setup, we also porivde configuration files for our boards.

## Setup ESPHome in Home Assistant

You can follow the [official guide](https://esphome.io/guides/getting_started_hassio) to install the ESPHome Add-on for Home Assistant.

The main steps are:

1. Open your Home Assitant UI
2. Go to Settings->Add-Ons->Add-on Store and search for ESPHome
3. Install and activate the ESPHome addon

## Setup the board in Home Assistant

1. Open ESPHome in Home Assistant
2. Connect your board only via usb to your PC
3. Click "New Device" and enter a name
<img width="409" alt="image" src="https://github.com/user-attachments/assets/c01adb14-b041-4001-88d8-c1de9aa4d283">

4. Click ESP32-S3
<img width="412" alt="image" src="https://github.com/user-attachments/assets/2f96c7cd-9611-45e3-ac7b-9eef8695aa58">

5. Copy and save the displayed encryption key and click skip
<img width="412" alt="image" src="https://github.com/user-attachments/assets/0601f882-b53e-445d-bc7c-b402f84b355b">

6. Click on the secrets button on the top right, create the following keys and enter your wifi credentials as well as the secret api key you just copied, hit save

```
wifi_ssid: "myWifi"
wifi_password: "myWifiPassword"
api_key: "myApiSecretWeCopiedAfewMinutesAgo"
web_username: "admin"
web_password: "tynet.eu"
hcp_wifi_ap_password: "tynet.eu"
```

7. Click Edit on the device card
<img width="404" alt="image" src="https://github.com/user-attachments/assets/0c3b92ee-bd92-488f-8b1d-f8b9932b61c1">

8. Copy paste the content of the esphome.yaml file from this repo into the editor, click save
<img width="857" alt="image" src="https://github.com/user-attachments/assets/d6283427-480f-4128-8c11-9a84b51699a7">


9. Click install, then select Manual download, wait for the firmware to be build, select factory image to get the.bin file
<img width="1070" alt="image" src="https://github.com/user-attachments/assets/bc316b5e-8e84-47a2-a0fb-bd4f69eaa117">
