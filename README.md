# current build

The current LeanDog MakerGear M2 build:

* 2014 MakerGear M2 with:
  * 24v power supply
  * silver + black Z motor
* Reinforced heated bed upgrade
* Dual Extruder upgrade
* 4-point bed upgrade
* M3 RAMBO addon board with Raspberry Pi running Octoprint

# firmware

Current firmware base is [M2E-Production-SnNRd-V105](http://makergear.wikidot.com/local--files/m2-firmware/M2E-Production-SnNRd-V105.zip) with changes specific to dual extrusion pulled from the dual extruder firmware. There's also a slight tweak to Z-height for build dimension to adjust for the way we set up the z endstop with the old-style z motor.

# flashing

~~Arduino 1.5.5 is in the repo, which should be used for flashing. Select MEGA
2560 as board. You do not need the RAMBo-specific board library.~~

UPDATE: Flashing should be done instead via [platform.io](http://www.platformio.org).
Instructions need to be added.

# z offsets

Borosilicate + PEI: -3.55

To read EEPROM settings:

```
M503 ; echo settings from EEPROM to serial output
```

To set Z offset:

```
M206 Z-3.55 ; sets z offset to -3.55
M500 ; save to EEPROM
```
