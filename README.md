# micropython-smbus
A wrapper to provide methods of the CPython 'smbus' module on micropython

Provides an 'SMBus' module which supports some of the py-smbus i2c methods, as well as being a subclass of machine.I2C 

Hopefully this will allow you to run code that was targeted at py-smbus, unmodified on micropython.
 
# Usage
Use it like you would the machine.I2C class: 
    
            import usmbus.SMBus 
            bus = SMBus(SMBus.MASTER, pins=('G15','G10'), baudrate=100000)
            
            # Example for the bme680:
            bme680.BME680(i2c_device=bus)

## Work In Progress
This module came from a desire to use https://github.com/pimoroni/bme680 on a LoPy, so currently implements only the methods necessary to do that. 

I'll be adding more as time goes on: issues/pull requests are very welcome.
