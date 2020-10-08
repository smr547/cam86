# Design notes

A page devoted to miscellaneous design notes

## Horizontal driver

One aspect of the present CAM86 design is the bit-banging approach for generating the clocking for the horizontal shift register and the ADC clocks. 
Whilst there is some hardware dedicated to generating the USB FIFO write pulse (WR#) and the Reset Gate pulse (RG), the majority of the timing is
driven by free-wheeling software. There is no use of timer/counter hardware or interrupt routines.

The upside of this design is simplicity of hardware. The downside is heavy use of CPU and potential timing jitter if external events need to be serviced
(e.g. command channel servicing or temperature control).

An improved design would involve

* External crystal oscillator (at say, 32MHz) -- [Pierce Oscillator design video](https://www.youtube.com/watch?v=5StwZCeNzVU)
* divide by two D-flip/flop to provide 16MHz clock (fed to uProc) -- see [Divide by 2 tutorial](https://www.electronics-tutorials.ws/counter/count_1.html)
* [MUX](https://www.ti.com/lit/ds/symlink/cd74hct253.pdf?ts=1601865485514&ref_url=https%253A%252F%252Fwww.google.com%252F)
to provide 90 and 180 degree phase shifted clocks for ADC (see [this post](https://electronics.stackexchange.com/questions/310627/two-phase-clock-on-a-breadboard))
* Timer/Counter1 and ISR to generate vertical timing signals

Generating the horizontal and ADC clocks in hardward removes jitter and frees the CPU for higher level tasks (e.g. closer temperature monitoring, 
immediate command response)

See also:

* [Commercial clock driver cards](http://www.pulseinstruments.com/drivers/)

## Electronic shutter

A high voltage pulse on the SUB pin is used to clear photo-electrons from the photodiodes immediately before the start of an exposure. Care must be taken
to [prevent SUB pulses in bright light conditions](https://www.onsemi.com/pub/Collateral/AND9183-D.PDF) that might damage the CCD component.

## CCDs

* [Theory of operation](https://www.chem.uci.edu/~unicorn/243/handouts/243Photodiodes.pdf)
* For a more ambitious project consider the [KAF-16803 sensor](https://www.onsemi.com/pub/Collateral/KAF-16803-D.PDF) 
available at a [reasonable price from Mouser](https://au.mouser.com/ProductDetail/863-KAF16803ABA-DDAE)


