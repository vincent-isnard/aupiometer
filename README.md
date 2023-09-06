# The Aupiometer
The Aupiometer: an open-source audiometer with Raspberry Pi

Installation of Patchbox:
-------------------------
1) Download and install Patchbox-os on your computer: https://blokas.io/patchbox-os/
2) Download and install balenaEtcher: https://etcher.balena.io/
3) Insert a SD card: "Flash from file" and select the Patchbox image.
4) Click on "Select target" and select the SD card.
5) Click on "Flash" (~5 min; "Flash failed").
6) Copy the Aupiometer folder at the root.
7) Eject the SD card.

Configuration of Patchbox:
--------------------------
1) Insert the SD card on the Raspberry Pi.
2) Connect a keyboard, a sound card and headphones, and plug the Raspberry Pi to power supply to start it.
3) Enter login and password.
4) During the configuration, choose: "v10 USB" as sound card, 48 kHz, 128, 2.
5) Choose boot environment: "desktop autologin".
6) Choose module: "puredata".
7) Choose option for autolaunch: "Cancel".
8) Start: "startx".
9) Invert the touchscreen: "sudo nano /boot/config.txt" in the terminal, remove "#dtoverlay=vc4-fkms-v3d" and add "lcd_rotate=2".

Configuration of the Pure Data patches:
---------------------------------------
1) Copy the Aupiometer folder in the folder "/usr/local/puredata-patches".
2) Add the folders in the Pure Data paths.
3) Reconfigure Patchbox for automatic start of the patch: "patchbox" in the terminal, and select the same options than previously except "Option for autolaunch": select "main.pd", which corresponds to the main patch of the Aupiometer.
