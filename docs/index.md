# Overview

Information about HackerLab V3 Hardware badge. On June 22, 2019 we hosted our anual HackerLab [@Engine4](https://twitter.com/engine4cws/) in Puerto Rico. Our HackerLab main goal is to provide a space for hackers to play and learn about different aspect of security specially IOT stuff.
As part of our activity, every (well almos everyone) participant takes home a special hardware badge for them to play, hack or do what ever they want with them. And this is the place to find the information about such fantastic piece of hardware. Enjoy and feel free to comment on our github [project repo](https://github.com/soynerdito/RickBadge).

# HackerLab V3 Keynote
During the HackerLab V3 we had a keynote about #badgelife and our RickBadge. Pdf for slides can be found on [HackerlabV3_Keynote_2019.pdf](https://github.com/soynerdito/RickBadge/raw/master/References/HackerlabV3_Keynote_2019.pdf).


# Design files

All design files are open source and free for everyone to download modify and make their ouwn from our [Github repo](https://github.com/soynerdito/RickBadge "Badge Repo"). The making of this badge was done using free open source tools like, KiCad, LibreCad and Inkscape. And of course the help of one or two seach engines and Youtube as always.
Components were source from ebay and making of the actual PCB board was done in China. All soldering was a labor of love with a soldering iron and patience.

First design sent to fabrication looked like this. This are KiCad renderings of the board before being manufactured.

![Board 3D](img/rick3dblue.png)

![Back Side](img/rick3dblue_back.png)

# Components
All Components are [smd components](https://en.wikipedia.org/wiki/Surface-mount_technology) specially 0603 size as they are easier to solder by hand.
Bill of material is:

Qt | Part Number | Description | Footprint
-- | ----------- | ----------- | ---------
7 | Led | Regular Led | 0603
8 | 680 Ohm | Resistor | 0603
1 | 12K Ohm | Resistor | 0603
1 | 10uF | Capacitor | 0603
1 | | Slide switch |
1 | CR2032 | 3V coin cell battery |
1 |  | Baterry Holder for CR2032 |
1 | Attiny13A | Atty micro controller | SOP8
1 | 74HC164 | 8 bit Shift register | SOIC14


# Programming
THe Rick Badge is fully programmable as it has an ATtiny13A microcontroller. It has a small flash space to hold a program but it can be programmed with no problem. As the microcontroller is part of the former Atmel family. It can be programmed using traditional atmel programming tools or Arduino IDE. Thanks to the internet all the hard work has been done by others and shared. You can use any search for "How to program Attiny13 using Arduino" and will find a lot of tutorials. Due to changes on the Arduino IDE some tutorials stop working after an upgrade. It is not that the language or compilter is not compatible, problems I have seen are because of the file format that describes the board changes from one version to another. Enought writing lets get this doing.

## What I did
!!! note "Note:"
    Full Guide can be found at:

        Full guide at http://highlowtech.org/?p=1695
### Sumamry
+ Download Arduino IDE from official page
- Open Arduino Ide File->Preferences
- Add this to "Additional Boards Manager URL:" https://raw.githubusercontent.com/damellis/attiny/i de-1.6.x-boards-manager/package_damellis_attiny_index.json
* Done!
### Hardware
In order to download code to the rick badge an external programmer is required. Either using an Arduino as ISP or with another programmer like a usbASP programmer. External programmers are cheap but if you already have an Arduino UNO and a capacitor you have a programmer.

### Before coding
Microcontrollers out of the factory come with default settings for speed and usage. This may or not be what you desire. For example if you need a microcontroller for a particular use or internal clock speed a one time configuration must be done.
An easy way to do this is just by selecting Burn Bootloader option from the Arduino IDE.
![Configure Chip](burn_bootloader.png)

## Sample Code
A simple sample code for the Rick Badge can be downloaded from 
https://github.com/soynerdito/RickBadgeSampleCode




# Making my own badge

# References
