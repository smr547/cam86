## Compiling the Firmware

* Forked the [original firmware repo](https://github.com/axsdenied/cam86_fw) to [my repo](https://github.com/smr547/cam86_fw)
* Cloned [my forked repo](https://github.com/smr547/cam86_fw) to local Raspberry Pi computer ``/home/smr/projects/cam86_fw``
* [Loaded the AVR toolchain](https://github.com/NicoHood/NicoHood.github.io/wiki/How-to-(cross-)compile-AVR-programs-with-Raspberry-Pi)
* Read [tutorial on AVR firmware programming](https://davecturner.github.io/2019/02/23/programming-avr-microcontrollers.html) 
* Firmware required [some tweeking](https://github.com/smr547/cam86_fw/commit/4b21ddc64c1e530558b1b4bb644aea4e3002d93a#diff-e259f5aede15bbde1e829fd71b20b474)
to allow it to be built with the [AVR toolchain](https://github.com/NicoHood/NicoHood.github.io/wiki/How-to-(cross-)compile-AVR-programs-with-Raspberry-Pi)
* On first successful compile, ``pixel1000`` macro expanded to produce a huge object file (approx 300KB) which was way too big for the ATMeg328 flash memory.
Any clues
* Modified the macros to [incorporate programmed loops](https://github.com/smr547/cam86_fw/commit/fa0dd519e622a44199ec0d2d5a90406b3ca708b4#diff-e259f5aede15bbde1e829fd71b20b474),
significantly reducing the memory footprint -- wondering if this will effect CCD readout timing possibly introducing artefacts? 
