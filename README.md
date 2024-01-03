GET STARTED

Install manually.  Follow https://esphome.io/guides/getting_started_command_line or https://esphome.io/guides/getting_started_hassio

See https://esphome.io/components/sensor/dht.html

I thought it would be necessary to add a 10kOhm pull-up resistor, but the device fails when I do that.  And it doesn't seem necessary to specify the internal pull-up in the pin config.  So simply add the following to the .yaml config file:

```
sensor:
  platform: dht
  model: DHT22
  pin: GPIO4
  temperature:
    name: "Temp"
  humidity:
    name: "Hum"
  update_interval: 5s
```

Save .yaml config to `./config` folder.

Build it:

```
esphome run config/ambient.yaml
```


Run the web dashboard and maintain it from there:

```
$ esphome dashboard config/
```

