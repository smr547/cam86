# cam86
Something I've been wanting to do for years! -- Build a CCD camera for astrophotography. 
The cam86, originating from a group of keen Ukrainian amateurs, looks like the perfect challenge. 

![The cam86 CCD camera](https://stargazerslounge.com/uploads/monthly_2019_02/1595828296_ScreenShot2019-02-23at11_20_20PM.jpg.4a7e144ca60858cb34bd007e59f116e9.jpg "Photo 1")

## This repo

* [Hardware](./hardware)
* [Software](./software)

## Online resources

cam86 is the last in a series of CCD cameras developed by collaborators coordinated by members of the Kiev Astronomical Club in the Ukraine. 

* [webastro forum](https://www.webastro.net/forums/topic/148427-camera-ccd-fabriqu%C3%A9-maison-cam86/) -- currently very active forum -- in French 
* [astroccd homemade CCD camera group](http://astroccd.org/2016/10/cam86/) -- last posting late 2016
* [CloudyNights forum](https://www.cloudynights.com/topic/497530-diy-astro-ccd-16-bit-color-6mpx-camera/) -- a lengthy forum in English -- last post July 2020
* [StarGazers Lounge forum](https://stargazerslounge.com/topic/304166-diy-osc-ccd-cam86/) -- English forum -- some great pics -- last Post Jan 2019
* [Kiev Astronomy Club forum](http://www.astroclub.kiev.ua/forum/index.php?topic=28929.0) -- original developers forum in the Ukraine -- currently active
* [Australian forum](http://www.iceinspace.com.au/forum/showthread.php?t=146493) -- last post 2019
* [Firmware repo by Luka Pravica](https://github.com/axsdenied/cam86_fw) -- with lots of references to online resources
* [User manual from QYH project](http://www.gamaelectronics.com.au/files/QHY-8%20Users%20manual.pdf) -- uses same sensor as CAM86

[ASCOM](https://ascom-standards.org/Developer/Alpaca.htm) -- a set of "standards" for astronomical devices operating in a 
Windows environment. Thanks to RESTful and other network technologies the ASCOM "standard"
may become more relevant to the Open Source community

## Important update

After reviewing the available documentation I've decided not to proceed with this build

* The Ukrainian developers have moved onto a later design (CAM90)
* Documentation for SONY CCD chip has not been released by the manufacturer

Also, some design issue remain unaddressed in the CAM86

* banding in images, 
* noise from on board power supply, 
* noise from Peltier switching, 
* bitbang firmware, 
* Delphi drivers

I'll continue prototyping work towards building an imager based on the CAM87 or CAM90 design. 

Thank you again to the marvelous people working on these project. Their generosity together with the knowledge and experience they have shared with the community
remain invaluable. 
no flow control in USB Asynchronouse FIFO data channel
*
* 
