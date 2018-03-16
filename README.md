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

1. Clone latest firmware (*.bin) file from this repository.
2. Use `esptool.py` command to flash firmware into chipset.
3. Connect chipset to power supply.
4. After boot screen. Press `PRG` button for 2 seconds (until screen shown `AP Mode`). In this time, __Wi-Kit__ will switch into `Access Point` mode. You will found a new Wireless network nearby with name `Wi-Kit`.
5. Connect to `Wi-Kit` with default password: `12345678`.
6. After connect successfully, open _http://192.168.4.1_ to enter setup page.
7. On top menu, click on __Network Settings__.
8. Enter your SSID and wifi password, then click __Update__ to save.
9. Click on __Restart Device__ to restart __Wi-Kit__ or press `RST` button on board to hard restart device.
10. Now __Wi-Kit__ will connect to your wireless network, you're ready to go!


### Photos

![Homepage](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-homepage.png?raw=true)
![Network Settings](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-station.png?raw=true)
![General Settings](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-general.png?raw=true)
![Plugins](https://github.com/dphans/Wi-Kit/blob/master/screenshots/screenshot-plugins.png?raw=true)

