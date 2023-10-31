[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

# rru-rf-hw
Remote Radio Unit RF board.

<img src="https://github.com/M17-Project/rru-rf-hw/blob/main/m17-rru-rf.png" width="850">

## What is it?
An FM repeater in a milled aluminum chassis. Built around a pair of [CC1200 chips](https://www.ti.com/product/CC1200) from Texas Instruments and an RF power amplifier module.

## Quick fact sheet
RF power module - [RA60H3847M1]([https://www.mitsubishielectric.com/semiconductors/hf/products/lineup/index.html](https://www.mitsubishielectric.com/semiconductors/hf/products/datasheet/ra60h3847m1.pdf))<br>
RF output power - 60W<br>
Frequency range - 420..450MHz<br>
Frequency error - <0.5 ppm over -40 to +85°C range<br>
Supply voltage - 13.8V DC<br>
Power consumption - ~150W at 60W RF out<br>
Load mismatch immunity - continuous over the whole VSWR range (built in RF isolator)<br>
Harmonic content - 2nd <-35dBc, 3rd <40dBc (to be measured)<br>
Mode support: analog FM, AFSK (APRS), M17 (possibly others too)<br>

## License
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
