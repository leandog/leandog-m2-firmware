# firmware

Current firmware base is [M2E-Production-SnNRd-V105](http://makergear.wikidot.com/local--files/m2-firmware/M2E-Production-SnNRd-V105.zip)

# flashing

Arduino 1.5.5 is in the repo, which should be used for flashing. Select MEGA 2560 as board. You do not need the RAMBo-specific plugins.

# z offsets

Borosilicate + PEI: -4.05

To read EEPROM settings:

```
M503 ; echo settings from EEPROM to serial output
```

To set Z offset:

```
M206 Z-4.05 ; sets z offset to -4.05
M500 ; save to EEPROM
```
