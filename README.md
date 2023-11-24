# KIM-1 RAM/ROM Expansion Board for the MTU Backplane

## About

This is a highly configurable RAM/ROM expansion for MTU backplanes, like the one in the original K-1005 card file, my [expansion card](https://github.com/eduardocasino/kim-1-mtu-expansion-card) or my buffered motherboard.

WARNING: This design has not been tested yet. Use at your own risk!

## Characteristics

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

## Changelog
#### 24/11/2023
* Add option to support the MTU floppy controller boot prom 

## Acknowledgements

* This design is based on late Bob Applegate's [60K RAM/ROM card](https://www.corshamtech.com/product/kim-1-60k-rameprom-board/)