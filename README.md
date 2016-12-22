# homebridge-system-plugin

Homebridge plugin which make system calls when the switch is turned off or on.
The exact system calls need to be specified in the homebridge config file (see
sample config below).

I am using this to control:
- Elekcity RF 433 MHz switches
- My TV using IR Emitter with lirc


Sample Config:
---------------
In "accessories" section in homebridge config:
~~~~
{
  "accessory": "systemCallAccessory",
  "name": "Bedroom Tubelight",
  "on_system_call": "/home/pi/rf/rfoutlet/codesend 349635 -p 2 -l 203",
  "off_system_call": "/home/pi/rf/rfoutlet/codesend 349644 -p 2 -l 203"
}
~~~~
