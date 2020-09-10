

## Power Supply
* Multiple voltages from 12V input
* Designed around [MAX743](https://datasheets.maximintegrated.com/en/ds/MAX743.pdf)
## CCD Sensor
* Uses a ICX453AQ 6M pixel colour CCD sensor from Sony. 
* Unfortunately Sony has not published a datasheet for this sensor but the [ICX413](http://www.opticstar.com/Download/Astro/Doc/Imagers/CCD/Sony/ICX413AQ.pdf)
is said to be similiar.
* There has been a significant effort to reverse engineer the specs fo the ICX453AQ and I'll try to collate the findings here.
 * [some discussion here](https://www.cloudynights.com/topic/497530-diy-astro-ccd-16-bit-color-6mpx-camera/page-7)
## ADC
* Analog Devices [AD9826](https://www.analog.com/media/en/technical-documentation/data-sheets/AD9826.pdf) 16 bit analog to digital coverter
## Vertical Clock driver
* Sony [CXD1267](http://pdf.dzsc.com/CXD/CXD1267AN.pdf)
## Horizontal driver
* [EL7457](https://www.renesas.com/us/en/products/amplifiers-buffers/all-amplifiers/powerfet-ccd-drivers/device/EL7457.html)
## USB interface
* [FT2232](https://au.mouser.com/datasheet/2/163/DS_FT2232H-1621240.pdf)
* [93C46](http://ww1.microchip.com/downloads/en/DeviceDoc/doc5140.pdf) EEPROM for USB id and configuration
* [Evaluation module](https://datasheet.octopart.com/FT232BL-REEL-FTDI-datasheet-7829588.pdf)
* The USB interface appears to operate in asynchronous FIFO mode as outlined in this 
[technical note](https://www.ftdichip.com/Support/Documents/TechnicalNotes/TN_167_FIFO_Basics.pdf)
## Microprocessor
* [ATMeg328](http://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-7810-Automotive-Microcontrollers-ATmega328P_Datasheet.pdf)
## Miscellaneous logic
* Quad XOR gates [74H86](74HC86.PDF)
