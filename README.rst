Introduction
============

A micropython library for the VCNL4040 proximity and ambient light sensor.


Installing 
=============
Copy vcnl4040.py to the board.

Usage Example
=============

.. code-block:: python

    from machine import Pin, I2C
    import vcnl4040

    i2c = I2C(scl=Pin(21), sda=Pin(22))
    sensor = vcnl4040.VCNL4040(i2c)
    
    while True:
        print("Proximity:", sensor.proximity)
        print("Light: %d lux" % sensor.lux)
        time.sleep(1.0)


