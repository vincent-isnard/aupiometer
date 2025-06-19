# The Aupiometer
The Aupiometer: an open-source audiometer with Raspberry Pi

## Changelog
### Version 0.7 (June 19, 2025)
1) [All] New display ergonomics (with kiosk-plugin) and a configuration file to save the settings.
2) [Home page] Added a switch button to choose the language (French or English).
3) [Pure-tone audiometry] Added the 63 Hz frequency with 25 dB more than for 125 Hz (cf. Moller & Pedersen, 2004). /!\ Not calibrated with participants.
4) [Pure-tone audiometry] Added a calibration module accessible in the configuration module where the calibration values ​​are set (or directly accessible from the 'externals' folder).
5) [Pure-tone audiometry] Added a graphics module to plot the audiogram.
6) [Speech audiometry] Added speech audiometry test interfaces (digits, logatomes, MRT, CRM). /!\ Not calibrated with participants.
7) [Tinnitus] Added Tinnitus Handicap Inventory (Newman et al., 1996) and visual analogue scales (Ohresser, 2017).
8) [Hyperacusis] Added Hyperacusis Questionnaire (Khalfa et al., 2002) and visual analogue scales (Fernandez & Isnard, in preparation).
9) [15iSSQ] Added Speech, Spatial and Qualities of Hearing 15-item questionnaire (Ferschneider et al., 2022).

## Installation of the Aupiometer
### Installation of Patchbox
1) Download and unzip Patchbox-os on your computer [tested with version 2022-05-17 for Pi 3B+]: https://blokas.io/patchbox-os/
2) Download and run balenaEtcher on your computer [tested with version 2.1.2]: https://etcher.balena.io/
3) Insert a SD card: "Flash from file" and select the Patchbox image, then select the SD card.
5) Click on "Flash" (~5 min).
6) Copy the Aupiometer folder at the root.
7) Eject the SD card.

### Configuration of Patchbox
1) Insert the SD card on the Raspberry Pi.
2) Connect a keyboard, a sound card and headphones, and plug the Raspberry Pi to power supply to start it.
3) Enter login (patch) and password (blokaslabs).
4) During the configuration, choose: "v10 USB" as sound card, 48 kHz, 128, 2.
5) Choose boot environment: "desktop autologin".
6) Choose module: "puredata".
7) Choose option for autolaunch: "Cancel".
8) Start: "startx".
9) Invert the touchscreen: "sudo nano /boot/config.txt" in the terminal, remove "#dtoverlay=vc4-fkms-v3d" and add "lcd_rotate=2".

### Configuration of the Pure Data patches
1) Copy the Aupiometer folder from "boot" folder in the folder "/usr/local/puredata-patches".
2) Launch Pure Data and add all the folders in the Pure Data paths.
3) Reconfigure Patchbox for automatic start of the patch: "patchbox" in the terminal, then "wizard", and select the same options than previously except "Option for autolaunch": select "main.pd", which corresponds to the main patch of the Aupiometer.

## Reference
Isnard, V., Chastres, V., & Andéol, G. (2024). Description of a new low-cost and open-source audiometer and its validation with normal-hearing listeners: The Aupiometer. Plos one, 19(8), e0306751. [with Aupiometer version 0.6]
