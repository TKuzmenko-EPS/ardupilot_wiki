.. _common-cuav-pwlink:
[copywiki destination="plane,copter,rover,blimp,sub"]
============
CUAV PW-Link
============

.. image:: ../../../images/cuav-pwlink.jpg


CUAV PW-LINK is an ESP8266 based 2.4Ghz WIFI telemetry radio. It connects to any ArduPilot telemetry port using +5V,gnd,TX and RX signals. Running at the standard default parameters of 57.6 Kbaud and MAVLink2 telemetry protocol, it connects via the standard Mission Planner/ QGC UDP port 14550 over WIFI. 

With its external antenna, range of 450 meters is typical. 

.. image:: ../../../images/pwlink-system.jpg

Connecting to the Ground Station
================================

Open WIFI connection dialog on PC or Android Phone and select the ``CUAVWLINKxxxx`` SSID and connect using the password ``cuavwlink``. Once connected use the UDP connection with port = 14550 (which is default) to connect using Mission Planner. QGC should auto-detect and connect.
The PW-LINK default IP address is ``192.168.4.1``.


MAVProxy
--------

The following command can be used to connect a MAVProxy ground station to the vehicle.

.. code-block:: bash
  
    mavproxy.py --master :14550

More information
================

`CUAV docs <https://doc.cuav.net/data-transmission/pw-link/en/>`__.