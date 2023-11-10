# ESPHome USB Power Delivery Integration

Integration of the FUSB302 power delivery controller in ESPHome.


## Suggested hardware
A fully integrated ESP32-based peripheral board including USB Power Delivery is ready and coming soon! The board features various dedicated connectors for an OLED display, I2C and SPI peripherals using the Adafruit Industries and SparkFun sensor pinout convention, exposed assignable pins (meaning all pins of the ESP32 are used) and a 32 W analog output with PWM control for connecting fans with a standard 3 or 4 pin connector. This library has been tested on that board and confirmed to be USB PD capable according to the capabilities of this library.


## How to use

``` yaml
# Include the following in your ESPHome <config>.yaml
external_components:
  - source:
      type: git
      url: https://github.com/groothuisss/esphome-usb-powerdelivery.git
      ref: master
    components: fusb302


fusb302:
  maximum_supply_voltage: 9v # Change to the correct maximum supply voltage: [5v, 9v, 12v, 15v, 20v]
  interrupt_pin: GPIO36 # Change to the correct GPIOxx
```
