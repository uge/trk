# nrf9151 based picoballoon tracker in kicad

This repo contains a KiCad 8.0 project which hopes to implement a low power tracker for pico-balloons
based on the nRF9151 module and a WSPR protocol modulator.

## Why the nRF9151?

The nRF9151 is marketed with emphasis on cellular data and GPS capabilities with optimization for power.
Trackers are one category of intended applications and the device and software stack have provisions for 
aggressive power saving modes. Even if the cellular data connectivity feature is not used, the nrf9151
is a power efficient microcontroller with an embedded GPS.

The cellular functionality opens up the possibility of eventually using NTN services such as Skylo or Starlink.

## WSPR modulator

The Si5351 is a common frequency synthesizer used to implement the WSPR protocol. This design opts
for the TI CDCE6214 in hopes of reducing power consumption and to try something different.

## Power conversion

Following the Traquito's example, this design uses buck-boost converters to adapt to varying and lower voltages.
This design uses the TI TPS631010 which can operate at input voltages from 1.6V to 5.5V. There are two
buck-boost converters for the 1.8V and 3.3V supplies respectively.

## Manufacturing

This design is targeted at JLCPCB 4 layer design rules and includes JLCPCB part numbers in the BOM.
