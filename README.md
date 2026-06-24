# OpenAmigaVideoHybrid-04
OpenAmigaVideoHybrid-04 is a fork from SukkoPera's [OpenAmigaVideoHybrid](https://github.com/SukkoPera/OpenAmigaVideoHybrid) which is an Open Hardware implementation of revision-03 of the Video Hybrid integrated circuit used in some Commodore Amiga computers (Commodore Part No. 390229-03).
This fork is a new reversion (revision-04) optimized for automatic assembly at JLCPCB.

### Summary
The *Video Hybrid*, also known as *VIDIOT*, is a hybrid integrated circuit acting as a Digital-to-Analog Converter (DAC), which converts the digital 4-bit per color video signal of the Amiga into standard (analog) signals suitable to drive a monitor or TV.

It is used in Amiga models A500, A500+, A1000, A2000 and A3000. The Amiga 3000 actually uses two Hybrids: one for the 15kHz video output from Denise and one for the 31kHz video output from Amber. Two Hybrids are also used in the [GBA1000 A1000 Clone](https://www.amigawiki.org/doku.php?id=de:models:gb_a1000).

It is also used in some add-on cards, such as the [Commodore A2320 Deinterlacer](https://amiga.resource.cx/exp/a2320).

The Video Hybrid is a reliable component that usually "just works", but if it gets damaged there is no way of repairing it, the only option is to replace it.

### Architecture
The Video Hybrid has 5 sections, one for each of the red, green and blue colors, one for the synchronization signal and one for a composite monochrome signal.

The red, green and blue sections are identical: first, the digital signals are mixed together using the typical *binary-weighted resistors* DAC configuration. After that, the level of the resulting signal is amplified through an NPN transistor. At the output, the signal is terminated at 75 ohms, as is typical for video signals.

The composite signal is generated in a similar way. The only significant differences are that the weighting resistors have different values and that the amplifier has two stages (NPN + PNP), in order to achieve a higher gain.

The synchronization signal is digital by nature, thus it needs no conversion, only some amplification.

### Building
The board is optimized for production at JLCPCB using theit basic part library. All LCSC# partnumbers are included in the design. Check the releases for gerbers, BOM and schematics.

### License
OpenAmigaVideoHybrid is Open Hardware. If you make any modifications to the board, please contribute them back.

### Disclaimer
OpenAmigaVideoHybrid is provided to you ‘as is’ and without any express or implied warranties whatsoever with respect to its functionality, operability or use, including, without limitation, any implied warranties of merchantability, fitness for a particular purpose or infringement. We expressly disclaim any liability whatsoever for any direct, indirect, consequential, incidental or special damages, including, without limitation, lost revenues, lost profits, losses resulting from business interruption or loss of data, regardless of the form of action or legal theory under which the liability may be asserted, even if advised of the possibility or likelihood of such damages.


### Thanks
- [Sukkopera](https://github.com/SukkoPera) for making the OpenAmigaVideoHybrid.

