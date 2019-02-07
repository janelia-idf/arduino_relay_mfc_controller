============================
arduino_relay_mfc_controller
============================

arduino_relay_mfc_controller is a python package to control the
Arduino relay mfc controller over USB, using the python module, the
command line, or a webpage using a webserver.


Install
-------

See INSTALL.rst

Python Module
-------------

Typical usage often looks like this::

    from arduino_relay_mfc_controller import ArduinoRelayMfcController, ArduinoRelayMfcControllers

    relay_mfc_controllers = ArduinoRelayMfcControllers()
    device_count = len(relay_mfc_controllers)
    if device_count == 0:
        raise RuntimeError('No Arduino relay mfc controllers detected, check connections.')
    valve_count = relay_mfc_controllers[0].valve_count
    mfc_count = relay_mfc_controllers[0].mfc_count

    o = ArduinoRelayMfcControllers[0]
    o.setMfcFlowRate(mfc=1,percent_capacity=75)
    print o.getMfcFlowRateSetting(mfc=1)
    print o.getMfcFlowRateMeasure(mfc=0)
    o.setRelayOn(4)
    o.setAllRelaysOff()

Web Page Controls
-----------------

Open a terminal and run::

    arduino_relay_mfc_controller_webserver.py

Open a browser and navigate to::

    http://localhost:5000


Author: Peter Polidoro

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
