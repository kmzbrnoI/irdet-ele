Infrared detector PCB
=====================

IR detector is an 8-input PCB allowing to sample signals from IR receiver
transistors. IR LED & IR fototransistor is placed near each other. This PCB
detects when signal fro emitter is received on receiver. It sends pulses to
emitter and checks for these pulses on inputs pins. Main aim of this PCB is to
smartly process signal from IR inputs so environment has no effect on inputs
states (e.g. intensity of lights).

This repository contains schematics & PCB layout of IRDET PCB. Firmware
for main MCU is available [here](https://github.com/kmzbrnoI/irdet-fw).

## Design

Schematics & PCB are designed in Eagle 9.

## Production

PCB is prepared to be automatically assembled in [JLCPCB](https://jlcpcb.com/).
SMD parts on bottom side should be assembled. Each SMD part has its `LCSC_ITEM`
attribute set.

## Parameters

 * Input voltage: 7–17 V.
   Protection: when > 18 V is applied, input is shorted. Afterwards, current
   is limited by PTC fuse on input to 200 mA. Changed-polarity protection.
 * Max current consumption: 150 mA.
 * Inputs: up to 8 IRs. Any number of IRs can be connected. Pulled up to +5 V
   internally. Capacitive coupling is used on inputs. No over-voltage protection.
 * IR LEDs: driver for each pair of IR LEDs. Short peaks of 100 mA stable current.
 * Logic outputs: galvanically separated from rest of PCB.

## Authors

The module is designed by Jan Horáček,
[Model Railway Club Brno](https://www.kmz-brno.cz/).


## License

Content of the repository is provided under [Creative Commons
Attribution-ShareAlike 4.0
License](https://creativecommons.org/licenses/by-sa/4.0/) as openhardware
project. You may download any data, contribute to the project, create PCB
yourself or even sell it yourself.
