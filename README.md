# KIM-1 RAM/ROM Expansion Board for the MTU Backplane

## **WARNING**

**ALTHOUGH THE REV. 3 SEEMS TO BE WORKING SO FAR, IT STILL NEEDS MORE TESTING. USE AT YOUR OWN RISK!!!**

If you ordered the first or second revision PCB, please see the "Rev. 1 Fix" and/or "Rev. 2 Fix" sections below.

## About

This is a highly configurable RAM/ROM expansion for MTU backplanes, like the one in the original K-1005 card file, my [expansion card](https://github.com/eduardocasino/kim-1-mtu-expansion-card) or my buffered motherboard.

WARNING: This design has not been tested yet. Use at your own risk!

## Characteristics

* Switchable 0000-03FF systen RAM replacement
* Switchable 0400-13FF RAM
* Switchable system ROM replacement (needs a small modification to the MTU boards to disable the DECEN line)
* 4 selectable ROM sets
* Enough room to place a ZIF socket for the ROM
* Switchable 4K RAM/ROM areas from 2000 to FFFF
* Configurable interrupt vectors to the top of any of the 4K chunks.
* Max. 1 TTL load on the bus, so it will work nicely on unbuffered backplanes

![components](https://github.com/eduardocasino/kim-1-mtu-ram-rom/blob/main/images/kim-1-RAM-ROM.png?raw=true)
![front](https://github.com/eduardocasino/kim-1-mtu-ram-rom/blob/main/images/kim-1-RAM-ROM-front.png?raw=true)
![back](https://github.com/eduardocasino/kim-1-mtu-ram-rom/blob/main/images/kim-1-RAM-ROM-back.png?raw=true)

## Licensing

This is a personal project that I am sharing in case it is of interest to any retrocomputing enthusiast and all the information in this repository is provided "as is", without warranty of any kind. I am not liable for any damages that may occur, whether it be to individuals, objects, KIM-1 computers, kittens or any other pets. **It should also be noted that everything in this repository is a work in progress, has not been tested and may contain errors, therefore anyone who chooses to use it does so at their own risk**.

[![license](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

See the LICENSE.md file for details.

## Rev. 2 Fix

Replacing the system RAM (0x0000-0x03FF) does not work reliably with the revision 2 PCB.

There is a simple fix with a couple of bodges:

Using a cutter, carefully cut the tracks that joins pin 24 of U1 and pin 16 of U2:

![step1](https://raw.githubusercontent.com/eduardocasino/kim-1-mtu-ram-rom/main/images/v2-fix-cut-front.png)

On the back side, cut the spoke at pin 24 of U1 (not strictly needed, but it is better to not have that copper island attached to the pin) and the track that joins pin 29 of U1 and pad 'V' of the edge connector:

![step2](https://raw.githubusercontent.com/eduardocasino/kim-1-mtu-ram-rom/main/images/v2-fix-cut-back.png)

Finally, solder these two wires:

![step3](https://raw.githubusercontent.com/eduardocasino/kim-1-mtu-ram-rom/main/images/v2-fix-wire-back.png)

## Rev. 1 Fix

If you built revision 1 of this board, you may have found out that the 0400-13FF RAM does not work with the [buffered motherboard](https://github.com/eduardocasino/kim-1-mtu-motherboard). It works fine with the [passive expansion board](https://github.com/eduardocasino/kim-1-mtu-expansion-card) and it should also work in a real MTU cabinet (See [Issue #1](https://github.com/eduardocasino/kim-1-mtu-ram-rom/issues/1))

You can perform this very simple bodge on the the PCB:

Using a cutter, carefully cut the track that joins pins 1 and 4 of U6 on the front side of the PCB:

![step1](https://raw.githubusercontent.com/eduardocasino/kim-1-mtu-ram-rom/main/images/fix-pcb-cut-front.png)

Now on the back side, cut these spokes at pins 12 and 13 of the same IC:

![step2](https://raw.githubusercontent.com/eduardocasino/kim-1-mtu-ram-rom/main/images/fix-pcb-cut-back.png)

Finally, solder these three wires:

![step3](https://raw.githubusercontent.com/eduardocasino/kim-1-mtu-ram-rom/main/images/fix-pcb-wire-back.png)

## Changelog
#### 30/04/2024
* Release Rev. 3
* Fix replacing system RAM
#### 28/01/2024
* Release Rev. 2
* Fix [Issue #1](https://github.com/eduardocasino/kim-1-mtu-ram-rom/issues/1)
* Add new option for replacing system RAM
* Make some more space for the ZIF socket lever
* Add instructions to fix Rev. 1 boards.
#### 05/01/2024
* Minor silkscreen modifications
#### 26/11/2023
* Remove useless option to support the MTU floppy controller boot prom
* Simplify design a bit
#### 24/11/2023
* Add option to support the MTU floppy controller boot prom
* Minor silkscreen update

## Acknowledgements

* This design is based on late Bob Applegate's [60K RAM/ROM card](https://www.corshamtech.com/product/kim-1-60k-rameprom-board/)