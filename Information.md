# Live DCS-BIOS
When enable DCSpy will use live/git version of DCS-BIOS. It is like DCS OpenBeta vs. Stable.

When you switch to live version for first time be patient DCSpy will download repository (ca. 150 MB it can take a few seconds), freeze can be expected.

This is recommended way by DCS-BIOS developers. 

DCSpy basically copy latest changes from DCS-BIOS repository into your `Save Games` folder, so every time you run DCSpy (when `Auto Update DCS-BIOS` is enable as well) latest commit form GitHub will be fetched.

Another option you can specify is `DCS-BIOS Git reference`, where `master` means latest commit. But you can use any branch or commit ID

![image](https://github.com/emcek/dcspy/assets/475312/7d1da9db-a123-456f-bf7a-78d70344ba8c)

![image](https://github.com/emcek/dcspy/assets/475312/f02d9027-abb5-4f54-924d-22d21730f811)

# FAQ
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

# Windows Defender
**Note**: Never trust anyone, download only from GitHub release page. Author of DCSpy do not take any responsible for users actions.

During download you can got into situation that Windows Defender will block it:

![image](https://github.com/emcek/dcspy/assets/475312/d6a5dfa1-7494-46dd-a568-925076f44831)

**It this case you need open, follow instructions**
1. Open Windows Security

![image](https://github.com/emcek/dcspy/assets/475312/8cf72801-d841-444c-87d5-37c7deb1413a)

![image](https://github.com/emcek/dcspy/assets/475312/60ce7c72-2b13-469e-8270-70dac03b8c28)

2. Open dropdown for latest issue

![image](https://github.com/emcek/dcspy/assets/475312/a5eb4770-3e5d-4d28-80a5-5c1c84a24bf4)  

3. Verify affected item name and select `Allow` from `Actions`

![image](https://github.com/emcek/dcspy/assets/475312/41a750ce-ef76-463c-a733-9715e3c125f5)  

4. Now download file should be possible, try again.

5. Additionally, you can try verify downloaded executable if is really DCSpy original file (not 100% foolproof)

6. Right click at downloaded file, open properties

![image](https://github.com/emcek/dcspy/assets/475312/f63b4a9b-9c64-4099-b6dd-0ffd02f7f4a4)

7. Go to [Actions](https://github.com/emcek/dcspy/actions)

![image](https://github.com/emcek/dcspy/assets/475312/a0d88222-618a-4bd5-b130-2f8c1e644ac5)

8. Verify numbers form point 6 and 7 should match (here `#101` - build number and `5295cca` commit ID)

# New ideas
I have lots of plans and new ideas how to improve it internally and form user's perspective, but don't hesitate to contact me. Maybe it will motivate me to implement some new stuff. Please open issue if you find bug or have any crazy idea.  
You are welcome [dcspy Discord](https://discord.gg/SP5Yjx3) server. 

# Credits
This project has been heavily inspired by [specelUFC](https://github.com/specel/specelUFC), and I want to thank **specel**, the author of that project for his work and the inspiring ideas. This software uses:
* [DCS-BIOS](https://github.com/DCSFlightpanels/dcs-bios) fork by DCSFlightpanels for exporting data from DCS to local network
* [jboecker's parser](https://github.com/jboecker/python-dcs-bios-example) to read data stream from DCS-BIOS
* The FontStruction [FalconDED](https://fontstruct.com/fontstructions/show/1014500) by 'uri_ba' is licensed under a [Creative Commons Attribution Non-commercial Share Alike](http://creativecommons.org/licenses/by-nc-sa/3.0/) license

# Contributing
You want contribute, perfect see: [contributing](https://github.com/emcek/dcspy/blob/master/CONTRIBUTING.md) guide.