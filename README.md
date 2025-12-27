# Psion-Organiser-Recreate-Mini
Files for the Psion Organiser Mini recreation

The repository structure:
<pre>

├── README.md
└── recovery
    ├── code
    │   ├── psion-mini-code
    │   │   └── mini-1-1-4-09.uf2
    │   └── UF2_bootloader
    │       ├── BOOT2350.uf2
    │       ├── bootloader_pico2.uf2
    │       └── diag_pico2.uf2
    └── sd-images
        └── a
</pre>

recovery
--------

The recovery directory contains enough files to get a Mini up and running.

code
----

The code directory contains files that can recreate the bootloader and Mini code on the Pico2.

UF2_bootloader
--------------

Thuis directory holds the UF2 bootloader files that allow UF2 files to be flashed from the SD card. This isn't stricty, necessary, as the Psion Mini UF2 can be flashed as the only 'application' on the Pico2. (If doing this after using the UF2 bootloader, the flash memory needs to be 'nuked', see the UF2 bootloader repository).

Instructions for the UF2 SD card bootloader and the code are here:

https://github.com/blackjetrock/psion-mini-uf2loader


psion-mini-code
---------------

This contains various Mini code versions, they are copied to the pico2-apps directory on the SD card and flashed using the UF2 bootloader. They can also be used as the only code on the Pico2, but using the UF2 bootloader is more flexible.

sd-images
---------

The directories here hold various images of the SD card and can be used to build an SD card for the Mini. The full test suite of OPL is in the images, but smaller sets of files can be used by omitting the test files.

