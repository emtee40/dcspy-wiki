## FAQ
1. Why in [F-16C DED](https://i.imgur.com/Hr0kmFV.jpg) instead of triangle up and down arrow I see strange character.   
   I didn't find good alternative, so I use unicode character [2666](https://www.fileformat.info/info/unicode/char/2195/index.htm) (I consider [2195](https://www.fileformat.info/info/unicode/char/2195/index.htm) as well, which do not render very well).
2. I got error: `'pip' is not recognized as an internal or external command, operable program or batch file.`  
   Probably during installation of Python `pip` and/or `Add Python to environment variables` were not selected. Uninstall Python and install again with correct options, or consider add Python installation directory to PATH environment variable.
3. Python 3.6 not supported due to 3 known vulnerabilities in Pillow library (version 9.0.0 drop support for Python 3.6)

| Name   | Version | ID            | Fix Versions |
|--------| --------|---------------|--------------|
| pillow | 8.4.0   | PYSEC-2022-10 | 9.0.0        |
| pillow | 8.4.0   | PYSEC-2022-9  | 9.0.0        |
| pillow | 8.4.0   | PYSEC-2022-8  | 9.0.0        |

4. DCSpy force using Python Imaging Library - Pillow 9.3.0 due to known vulnerability:

| Name   | Version | ID           | Fix Versions |
|--------|---------|--------------|--------------|
| pillow | 9.2.0   | OSV-2022-715 | 9.3.0        |

5. No data form DCS-BIOS issue:
  * You have to be in cockpit to DCS-BIOS sent any data to DCSpy
  * some VPN block LAN traffic - turn off Stay invisible on LAN

## New ideas
I have lots of plans and new ideas how to improve it internally and form user's perspective, but don't hesitate to contact me. Maybe it will motivate me to implement some new stuff. Please open issue if you find bug or have any crazy idea.  
You are welcome [dcspy Discord](https://discord.gg/SP5Yjx3) server. 

## Credits
This project has been heavily inspired by [specelUFC](https://github.com/specel/specelUFC), and I want to thank **specel**, the author of that project for his work and the inspiring ideas. This software uses:
* [DCS-BIOS](https://github.com/DCSFlightpanels/dcs-bios) fork by DCSFlightpanels for exporting data from DCS to local network
* [jboecker's parser](https://github.com/jboecker/python-dcs-bios-example) to read data stream from DCS-BIOS
* The FontStruction [FalconDED](https://fontstruct.com/fontstructions/show/1014500) by 'uri_ba' is licensed under a [Creative Commons Attribution Non-commercial Share Alike](http://creativecommons.org/licenses/by-nc-sa/3.0/) license

## Contributing
You want contribute, perfect see: [contributing](https://github.com/emcek/dcspy/blob/master/CONTRIBUTING.md) guide.