============================
Arduino Relay MFC Controller
============================

Arduino-based device to control 24V relays as well as Bronkhorst
IQFlow+ mass flow controllers.

A host PC can send the controller commands through a USB connection or
the controller can be operated standalone with 2 analog signals or 2
potentiometers.

BNC 0 controls the five relays.
0.25V : no relays on
0.75V : relay 0 on
1.25V : relay 1 on
1.75V : relay 2 on
2.25V : relay 3 on
2.75V : relay 4 on
3.25V : relay 5 on
3.75V : relay 6 on
4.25V : relay 7 on

BNC 1 controls the mfc 0 flow rate setting.
The flow rate is set as a percentage of the total mfc capacity.
If the mfc is rated as 1000 sccm, 20% capacity is 200 sccm.
% capacity = (voltage/5)*100
e.g.
0V   : 0%
0.1V : 2%
1V   : 20%
2V   : 40%
3V   : 60%
4V   : 80%
5V   : 100%

firmware
========

Contains the Arduino firmware files. See firmware/README.rst

host
====

Contains the code for controlling with a host computer.

python
------

See host/python/README.rst

pcb
===

Contains the pcb Kicad and gerber files.


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
