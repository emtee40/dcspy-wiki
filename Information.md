# Live DCS-BIOS
The easiest way to use this feature is from DCSpy, but you need [Git](https://git-scm.com/download/win) installed. It is possible download live version manually from GitHub and place in Save Games folder, but you need do it every time you want update latest changes of DCS-BIOS.

When enable DCSpy will use live/git version of DCS-BIOS. It is like DCS OpenBeta vs. Stable.

When you switch to live version for first time be patient DCSpy will download repository (ca. 150 MB it can take a few seconds), freeze can be expected.

This is recommended way using DCS-BIOS by its developers. 

DCSpy basically copy latest changes from DCS-BIOS repository into your `Save Games` folder, so every time you run DCSpy (when `Auto Update DCS-BIOS` is enable as well) latest commit from GitHub will be fetched.

Another option you can specify is `DCS-BIOS Git reference`, where `master` (recommended default value) means latest commit. But you can use any branch or commit ID.

Example:

![image](https://github.com/emcek/dcspy/assets/475312/7d1da9db-a123-456f-bf7a-78d70344ba8c)

![image](https://github.com/emcek/dcspy/assets/475312/5e088539-a086-4375-8e1e-161287a04f18)

# FAQ
1. Why in [F-16C DED](https://i.imgur.com/Hr0kmFV.jpg) instead of triangle up and down arrow I see strange character.   
   I didn't find good alternative, so I use unicode character [2666](https://www.fileformat.info/info/unicode/char/2195/index.htm) (I consider [2195](https://www.fileformat.info/info/unicode/char/2195/index.htm) as well, which do not render very well).
2. I got error: `'pip' is not recognized as an internal or external command, operable program or batch file.`  
   Probably during installation of Python `pip` and/or `Add Python to environment variables` were not selected. Uninstall Python and install again with correct options, or consider add Python installation directory to PATH environment variable.

3. No data form DCS-BIOS issue:
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

4. You can try restore quarantined file

![image](https://github.com/emcek/dcspy/assets/475312/7f2fb6bb-9be2-4af1-a073-8882ebd681c1)

5. or try downloading file again.

6. Additionally, you can try verify downloaded executable if is really DCSpy original file (not 100% foolproof)

7. Right click at downloaded file, open properties

![image](https://github.com/emcek/dcspy/assets/475312/f63b4a9b-9c64-4099-b6dd-0ffd02f7f4a4)

8. Go to [Actions](https://github.com/emcek/dcspy/actions)

![image](https://github.com/emcek/dcspy/assets/475312/a0d88222-618a-4bd5-b130-2f8c1e644ac5)

9. Verify numbers form point 6 and 7 should match (here `#101` - build number and `5295cca` commit ID)

# New ideas
I have lots of plans and new ideas how to improve it internally and form user's perspective, but don't hesitate to contact me. Maybe it will motivate me to implement some new stuff. Please open issue if you find bug or have any crazy idea.  
You are welcome [dcspy Discord](https://discord.gg/SP5Yjx3) server. 

# Credits
This project has been heavily inspired by [specelUFC](https://github.com/specel/specelUFC), and I want to thank **specel**, the author of that project for his work and the inspiring ideas. This software uses:
* [DCS-BIOS](https://github.com/DCS-Skunkworks/dcs-bios) fork by DCS-Skunkworks for exporting data from DCS to local network
* [jboecker's parser](https://github.com/jboecker/python-dcs-bios-example) to read data stream from DCS-BIOS
* The FontStruction [FalconDED](https://fontstruct.com/fontstructions/show/1014500) by 'uri_ba' is licensed under a [Creative Commons Attribution Non-commercial Share Alike](http://creativecommons.org/licenses/by-nc-sa/3.0/) license

# Contributing
You want contribute, perfect see: [contributing](https://github.com/emcek/dcspy/blob/master/CONTRIBUTING.md) guide.