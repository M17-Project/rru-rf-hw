[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

# rru-rf-hw
Remote Radio Unit RF board.

<img src="https://github.com/M17-Project/rru-rf-hw/blob/main/m17-rru-rf.png" width="850">

## What is it?
An FM repeater in a milled aluminum chassis. Built around a pair of [CC1200 chips](https://www.ti.com/product/CC1200) from Texas Instruments and an RF power amplifier module.
Revision A with CC1200 RF front-ends supports various FM-based modes, including M17 and AFSK.

## Quick fact sheet
RF power module - [RA60H3847M1](https://www.mitsubishielectric.com/semiconductors/hf/products/datasheet/ra60h3847m1.pdf)<br>
RF output power - 1..60W continuous, up to 80W with lower duty cycle<br>
Frequency range - 420..450MHz<br>
Frequency error - <0.5 ppm over -40 to +85°C range<br>
Supply voltage - 13.8V DC<br>
Power consumption - <150W at 60W RF out<br>
Load mismatch immunity - continuous over the whole VSWR range (built in RF isolator)<br>
Harmonic content - 2nd <-40dBc, 3rd <-55dBc (435MHz at 48.3dBm)<br>
Mode support: analog FM, M17, (A)FSK<br>
Circulator:  WH3538X-1, 400..470MHz (microstrip)<br>
Dummy load: Anaren [J100N50X4B](https://www.mouser.pl/datasheet/2/21/J100N50X4B-3364610.pdf)<br>

## Firmware
A basic, "crash-test" frmware template is available [here](https://github.com/M17-Project/rru-rf-fw).

## Chassis
Milled aluminum chassis is required. A reference design can be obtained from a [separate repository](https://github.com/M17-Project/rru-rf-chassis).

## Revision history
### Revision A
Initial revision.

### Revision B
* Switched mode voltage regulators have been replaced with linear.
* Added a buffer between the 40 MHz reference TCXO and transceiver ICs.
* Added bleeder resistors at the RF PA and 13.8V power supply.
* Slightly improved ALC circuit.
* Reduced N-connector cutouts (4.5mm down to 2mm).
* Added decoupling capacitor arrays at both RF PA's supply and VGG pins.
* DA15 connector now has MCU's BOOT0 signal available at pin 13.
* Bodge wire mod is no longer required, as both baseband trigger signals are now routed to the MCU.

### Revision C
* Added a lowpass filter after the RF PA stage
* Added a bandpass filter at the RF input
* TX and RX blocks are now clocked independently
* Pull-down resistor at TP2 (BOOT1)

## License
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
