# espruinohub-docker-rpi
Image docker with EspruinoHub  [A BLE -> MQTT bridge for Raspberry Pi and other Embedded devices] (https://github.com/espruino/EspruinoHub)

I forked the repository from hubertosales and changed the deprecated Node.js image hypriot/rpi-node to the official one from arm32v7/node.
This fork is not on docker hub, so a new image is created when running docker-compose up for the first time.

The resulting container was tested on a raspberry pi 4 running arch linux using this to get bluetooth running:
https://github.com/RoEdAl/alarm-bluetooth-raspberrypi

The errors about the unkown command sudo and/or setcap can be cleared by uncommenting the installation in src/dockerfile, 
however setcap does not seem to be required in order for bluetooth to work from inside the container.

# USAGE 

## Using docker-compose.yml (from repository)
``` 
 docker-compose up -d
```
