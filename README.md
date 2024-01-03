# ESPHOME-AMBIENT

This is an example esphome project to measure temperature, humidity, and pressure measurements with ESP32s.

## HARDWARE

Two hardware configurations are included in this project

### ambient-dht22

Adafruit ESP32 HUZZAH Feather with a DHT22 connected to GPIO Pin 4.

### ambient-bme280

Adafruit ESP32 HUZZAH Feather V2 with a BME280 sensor connected cia I2C.

## ESPHOME INSTALLATION

Getting started guides are [HERE](https://esphome.io/guides/getting_started_command_line) (command line) and [HERE](https://esphome.io/guides/getting_started_hassio) (web interface).

I prefer to install `esphome` manually and followed [THIS](https://esphome.io/guides/installing_esphome) installation guide.

## FIRMWARE

### Configuration File Creation

The configuration files provided this project were already created using the following process.

1. Create a subdirectory to hold your device configurations:

```
$ mkdir config
```

2. Create a new blank configuration file for each device.  You can run the command line wizard with, for example:

```
$ esphome wizard config/ambient-dht22.yaml
```

3. Edit the .yaml configuration file, adding the desired components and platforms associated with the device.

### Build and Upload to the Device

Build and upload each firmware to its respective device.  For example:

```
$ esphome run config/ambient-dht22.yaml
```

After it's running, you may run the web dashboard and maintain it from there:

```
$ esphome dashboard config/
```
