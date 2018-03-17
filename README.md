![Splash Screen](https://github.com/dphans/Wi-Kit/blob/master/logo.png?raw=true)

# Wi-Kit
__An IoT project using Heltec Wifi Lora 32 (ESP32), include useful online services.__


### Features

- Support both Wireless modes: `Station` and `Access Point`.
- Support web interface to control chipset (through _http://192.168.4.1_ in `Access Point` mode, or _IP Address_ of chipset in `Station` mode).
- Modularization the online services (aka plugins) like Weather service, Real Date and Time service,...
- Config Wireless network over web interface (in both `Access Point` mode and `Station` mode.
- Schedule to do some actions when time triggered (Cron-Job).


### To-Do

- Bluetooth ideas.
- Control via web-socket.
- ...


### Installation Instructions

- Clone latest firmware (*.bin) file from this repository then use [`esptool.py`](https://github.com/espressif/esptool) command to flash firmware into chipset:

```bash
git clone https://github.com/dphans/Wi-Kit.git
cd Wi-Kit
esptool.py --chip esp32 --port /dev/tty.SLAB_USBtoUART --baud 921600 --before default_reset --after hard_reset write_flash -z 0x1000 bootloader.bin 0x8000 partitions.bin 0xe000 boot_app0.bin  0x10000 wikit_firmware_*
cd ..
rm -rf Wi-Kit
```
Please note that need to change correct port of your USB connection. In bash script above, I'm using `/dev/tty.SLAB_USBtoUART`, it may be difference with your computer.

- Connect chipset to power supply.
- After boot screen. Press `PRG` button for 2 seconds (until screen shown `AP Mode`). In this time, __Wi-Kit__ will switch into `Access Point` mode. You will found a new Wireless network nearby with name `Wi-Kit`.
- Connect to `Wi-Kit` with default password: `12345678`.
- After connect successfully, open _http://192.168.4.1_ to enter setup page.
- On top menu, click on __Network Settings__.
- Enter your SSID and wifi password, then click __Update__ to save.
- Click on __Restart Device__ to restart __Wi-Kit__ or press `RST` button on board to hard restart device.
- Now __Wi-Kit__ will connect to your wireless network, you're ready to go!


### Photos

![Homepage](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-homepage.png?raw=true)
![Network Settings](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-station.png?raw=true)
![General Settings](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-general.png?raw=true)
![Plugins](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-plugins.png?raw=true)

