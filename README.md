## Home automation PCB

It will hold a series of breakout boards for I2C IO expanders, 1Wire drivers, ADCs. All are controlled with a Raspberry Pi 3B+.

This repo is mainly for reviewing purposes.


A list with the devices

### Relay board that will be driven:
https://www.sainsmart.com/products/16-channel-12v-relay-module

### 16 channel IO expander that will drive the board:
https://www.artekit.eu/products/breakout-boards/io/ak-pcf8575-i2c-16-bit-io-expander-breakout/

### I2C level shifter (3.3 to 5V)
https://www.pololu.com/product/2595

### I2C to differential signals:
https://www.sparkfun.com/products/retired/14589

### 1Wire drivers:
https://www.artekit.eu/products/breakout-boards/io/ak-ds2482s-100/

### ADC:
https://www.adafruit.com/product/1085

Some ADC "watch" only for presence/absence of 5V power but some are listenting to CT sensors.
Quasi similar model: https://www.seeedstudio.com/Non-invasive-AC-Current-Sensor-30A-ma-p-519.html



Add comments here (as git issues) or on EEVBlog.


