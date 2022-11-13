# Re-imagining the Color Computer 2
This hardware project started as an extension of learning PCB design skills now that production boards are a reality. I started with DSKY board, a weather station Raspberry Pi hat, and a business card sized sample circuit;  and was looking for a bigger challenge. While several of the 8-bit computers have been reproduced, the Tandy Color Computer has not. The closest is the Dragon, reimagined by Ciaran Anscomb. See below for my efforts to produce that board and get it working.
The design goal was to fit a Color Computer 2 case and use the non-vendor specific components. 
- The power supply was removed and replaced with a DC/DC Converter.
- Add the composite mod to replace the RF-Modulator (I did leave the connector in, but it may not be correct).
- Replacing the Dynamic RAM with modern Static RAM (AS6C4008).  I added connectors to allow for a daughter board to add the Dynamic RAM back in...which did create some pain in routing.
- Replace the Custom ROMs with a EEPROM (SST39SF040). There is a set of dip switches to allow for multiple versions of ROM code to be stored. I've laid that out so that a daughter board could be created to allow for the old ROMs to be used.
- The custom DAC and SALT chips were removed, and I used the Dragon circuits as a replacement. An early design had an AVR in place of the DAC. 
- I've added a place for an SDCard socket, which could be connected to Serial I/O or the Cassette lines on the PIA.
- I've removed the Cassette port.
One thing I want to do with a future version is to implement bank switching that is compatible to a CoCo3 or whatever can be done to make 2Mb of RAM available to OS/9 or NitrOS-9.


https://gitlab.com/sixxie/dragon64
https://github.com/danwerner21/Dragon64
