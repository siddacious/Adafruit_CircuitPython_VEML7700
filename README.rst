Introduction
============

.. image:: https://readthedocs.org/projects/adafruit-circuitpython-veml7700/badge/?version=latest
    :target: https://circuitpython.readthedocs.io/projects/veml7700/en/latest/
    :alt: Documentation Status

.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://discord.gg/nBQh6qu
    :alt: Discord

.. image:: https://travis-ci.com/adafruit/Adafruit_CircuitPython_VEML7700.svg?branch=master
    :target: https://travis-ci.com/adafruit/Adafruit_CircuitPython_VEML7700
    :alt: Build Status

CircuitPython driver for VEML7700 high precision I2C ambient light sensor.


Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_
* `Bus Device <https://github.com/adafruit/Adafruit_CircuitPython_BusDevice>`_
* `Register <https://github.com/adafruit/Adafruit_CircuitPython_Register>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://github.com/adafruit/Adafruit_CircuitPython_Bundle>`_.

Installing from PyPI
--------------------
On supported GNU/Linux systems like the Raspberry Pi, you can install the driver locally `from
PyPI <https://pypi.org/project/adafruit-circuitpython-veml7700/>`_. To install for current user:

.. code-block:: shell

    pip3 install adafruit-circuitpython-veml7700

To install system-wide (this may be required in some cases):

.. code-block:: shell

    sudo pip3 install adafruit-circuitpython-veml7700

To install in a virtual environment in your current project:

.. code-block:: shell

    mkdir project-name && cd project-name
    python3 -m venv .env
    source .env/bin/activate
    pip3 install adafruit-circuitpython-veml7700

Usage Example
=============

.. code-block:: python

    import time
    import board
    import busio
    import adafruit_veml7700

    i2c = busio.I2C(board.SCL, board.SDA)
    veml7700 = adafruit_veml7700.VEML7700(i2c)

    while True:
        print("Ambient light:", veml7700.light)
        time.sleep(0.1)


Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/adafruit/Adafruit_CircuitPython_VEML7700/blob/master/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.

Documentation
=============

For information on building library documentation, please check out `this guide <https://learn.adafruit.com/creating-and-sharing-a-circuitpython-library/sharing-our-docs-on-readthedocs#sphinx-5-1>`_.
