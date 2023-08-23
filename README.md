# ESP32-DMX-WiFi

Strongly based on amazing [LXDMXWiFi_Library](https://github.com/claudeheintz/LXDMXWiFi_Library) example [ESP32-DMX_rdm](https://github.com/claudeheintz/LXDMXWiFi_Library/tree/master/examples/ESP32-DMX_rdm).

Configuration utility for macOS and Windows is [here](https://github.com/claudeheintz/LXDMXWiFi_Library/tree/master/examples/configuration%20utility)

## Bill of materials

- DOIT ESP32 DevKit V1 30 pins board
- RS-485 transceiver like SN75176 or MAX485 or equivalent
  
## Schematic

```

RX2/GPIO16  ---+
               |                       
          3k   |    1k   +---------------+
GND  ---/\/\/\-+-/\/\/\--| R         VCC |---------- +5V (VIN when ESP32 board is powered by USB)
                         |               |
                    +----| RE/         B |---------- Data - (XLR pin 2)
                    |    |    SN75176    |
GPIO04      --------+----| DE          A |---------- Data + (XLR pin 3)
                         |               |
TX2/GPIO17  -------------| D         GND |---+------ Ground (XLR pin 1)
                         +---------------+   |
                                             |
                                             +
                                            GND
```


