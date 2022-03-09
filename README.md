## Home automation PCB

It will hold a series of breakout boards for I2C IO expanders, 1Wire drivers, ADCs. All are controlled with a Raspberry Pi 3B+.

The 220V actuators are controlled by a board with 16 mechanical relays. The board is in turn controlled by PCF8575 chip that takes I2C commands and controls 16 I/O pins. Board is active on low (optocouplers), PCF8575 can sink more current (than it could source). Perfect match.

The 16 relay board is separate, from this PCB, only a pin header connection is made.

The temperature sensors are DS18B20 that work on 1 wire protocol. These are already mounted with Ethernet cables terminated with RJ45. The sensors are read/driven by 4 ds2482s-100 chips (RJ45 terminals and ds2482s-100 are on this PCB).
The RJ jacks must be galvanic!

There are some other relays/contactors/voltages that needs monitoring, all done by 2 ADS1115 16-Bit ADC, present on board.

The chips are already sourced and live on their breakout boards. The PCB is mainly THT because of sourcing issues (eg can't find ds2482s-100 anywhere, will reuse existing breakouts). Only SMD are the 3.5 audio jacks (for ADC) again because no THT could be sourced atm.

The Raspberry Pi connector is only 20 pin wide because only the first few are used (5V, 3.3, SDA, SCL, GND)

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


