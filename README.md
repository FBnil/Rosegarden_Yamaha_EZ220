## Rosegarden Midi Instrument and Program definitions file for Yamaha EZ220

This is the Midi Bank definition for Rosegarden version 18.12 and up.
Currently it only has the Voices (and not the Drumkit).

### How to Install
The file is ready to be downloaded and can be put next to the other .rgd files in ~/.local/share/rosegarden/library/

### Procedure I followed

= Creating a RoseGarden file for the Yamaha EZ220
* First we download the pdf with all the instruments
https://usa.yamaha.com/files/download/other_assets/5/326995/ez220_en_om_a0.pdf
* Then we convert the pdf to html text, so it's a bit more workeable:
pdftohtml ez220_en_om_a0.pdf

* Then we follow the procedure described in:
https://www.rosegardenmusic.com/resources/documents/rgd-HOWTO.shtml

#### To know that MSB and LSB are:
https://www.sweetwater.com/sweetcare/articles/6-what-msb-lsb-refer-for-changing-banks-andprograms/

A true program change that also selects a bank is composed of (3) MIDI messages:
* CC 000 nnn (Bank Select MSB – Most Significant Byte)
* CC 032 nnn (Bank Select LSB – Least Significant Byte)
* Prog Change nnn (MIDI Program Change message 0~127)
