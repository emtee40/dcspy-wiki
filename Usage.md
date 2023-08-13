# Starting
## Single file download (new way)
1. Run Logitech Gaming Software (it allows accessing LCD)
2. Double click at downloaded file.
3. Click `Start`
4. LCD should update with dcspy basic info, waiting to connect to DCS 
5. Run DCS and start any mission.

## via pip (old way)
1. Run Logitech Gaming Software (it allows accessing LCD)
2. You can check with `pip uninstall dcspy` (**NOTE!** answer **No** to question) where dcspy was installed. Usually pip should install dcspy into your python directory: i.e.:
   * `c:\python311\lib\site-packages\dcspy-2.0.0.dist-info\*`
   * `c:\python311\lib\site-packages\dcspy\*`
   * `c:\python311\scripts\dcspy.exe`
   * `c:\python311\scripts\dcspy_cli.exe`
3. You can drag and drop `dcspy.exe` or `dcspy_cli.exe` to desktop and make shortcut (with custom icon, you can find icon in installation directory i.e. `c:\python311\lib\site-packages\dcspy\dcspy.ico`).
   * `dcspy.exe` - with open directly GUI window
   * `dcspy_cli.exe` - additionally start console window (with logs)
4. Double-click on dcspy icon or type `dcspy.exe`\`dcspy_cli.exe` from Command Prompt
5. Click `Start`
6. LCD should update with dcspy basic info, waiting to connect to DCS 
7. Run DCS and start any mission.

**Note:** DCS can already running, before starting LGS and or DCSpy.

**Note:** If you upgrade DCSpy before version 1.7.0 `dcspy.ico` and `config.yaml` were in data directory like `c:\python311\dcspy_data\` but location is deperched in Python if you still have it, you can safely delete it
# System tray icon
Since version DCSpy 2.1 you can minimalize it to system tray, using `X` (close) in main window

![image](https://github.com/emcek/dcspy/assets/475312/f90317ac-38a6-475b-a47c-325787b25b7d)

# Mono vs. Color
DCSpy do not use full potential of G19, which support full RGBA, 8-lines LCD with 7 programmable buttons.  
In contrast to mono devices (like G13, G15 and G510), which support mono, 4-lines LCD with only 4 buttons.  
Right now DCSpy use only top 4 lines of LCD and 4 buttons. 
Way in which actions assign to button for G13 (4 buttons form left to right) are mapped to G19 looks:  
* G13 1st button -> G19 left button
* G13 2nd button -> G19 right button
* G13 3rd button -> G19 down button
* G13 4th button -> G19 up button

## G13, G15, G510 - Mono
mono, 4-lines LCD with only 4 buttons  
![image](https://user-images.githubusercontent.com/475312/174407168-7db23a3f-3493-4a35-b898-ebb3a3ff839f.png)
![image](https://user-images.githubusercontent.com/475312/174407442-ed9c7d85-057d-4572-8316-3578721e4dab.png)
![image](https://user-images.githubusercontent.com/475312/174407530-b010691c-0895-4786-ad4e-8f98deeebb02.png)
## G19 - Color
full RGBA, 8-lines LCD with 7 buttons  
![image](https://user-images.githubusercontent.com/475312/174407299-d07e7ba5-d837-4af4-884a-7e20a48d676a.png)

Maybe in future when settings via config file will be added, then it allowed usage all 7 buttons in G19. But right now 
actions for supported airplanes are hardcoded right now.

# Configuration
All settings can be configured directly via GUI. However,  more advanced users can change configuration file `config.yaml` file. It is located in user's AppData directory (e.g. `C:\Users\<user_name>\AppData\Local\dcspy\config.yaml`). 
This is simple file, most users do not need to touch it at all. Configuring DCSpy enable some powerful features of DCSpy.

## Keyboards
![image](https://github.com/emcek/dcspy/assets/475312/e7e1ed0b-e76f-4c08-856b-a5eab32674cd)

* **keyboard** - default Logitech keyboard value, last used value is saved automatically  
  *possible values*: `G19`, `G510`, `G15 v1`, `G15 v2`, `G13`

## General
![image](https://github.com/emcek/dcspy/assets/475312/ed0a34be-0744-4001-99b8-9a16ba14368c)

* **autostart** - when set to `true` DCSpy start automatically.  
  *possible values*: `true` or `false`
* **show_gui** - it allows showing or hiding GUI during start of DCSpy. When set to `false` DCSpy start automatically.  
  *possible values*: `true` or `false`
* **check_ver** - check for new version during start of DCSpy.  
  *possible values*: `true` or `false`
* **dcs** - installation directory of DCS. By default it is set to `C:\Program Files\Eagle Dynamics\DCS World OpenBeta`
* **dcsbios** - location of DCS-BIOS folder inside user's `Saved Games\DCS.openbeta`.  
  Set this parameter to correct value allows user check and update DCS-BIOS to the latest release.  
  *example value*: `D:\Users\wags\Saved Games\DCS.openbeta\Scripts\DCS-BIOS`
* **theme_mode** - Theme mode
  *possible values*: system, light, dark
* **theme_color** - Color of widgets
  *possible values*: green, blue, dark-blue

## Mono
![image](https://github.com/emcek/dcspy/assets/475312/9a54cd03-36f4-496c-aeb0-bc33be956677)

* **font_mono_xs** - size of extra small font for mono devices
* **font_mono_s** - size of small font for mono devices
* **font_mono_l** - size of large font for mono devices
* **font_name** - file name with TrueType font use in all devices

## Color
![image](https://github.com/emcek/dcspy/assets/475312/0d44137b-71a8-495d-a66d-d3f04166950d)

* **font_color_xs** - size of extra small font for color devices
* **font_color_s** - size of small font for color devices
* **font_color_l** - size of large font for color devices
* **font_name** - file name with TrueType font use in all devices

## Special
![image](https://github.com/emcek/dcspy/assets/475312/a0fae074-083f-4112-a07f-2794d23f00b8)

* **f16_ded_font** - Special font for F-16's DED (G19 Color LCD only)

## Advanced
![image](https://github.com/emcek/dcspy/assets/475312/07f0cc15-4c4a-43c9-a3a0-9018a978723f)

* **save_lcd** - take every change of LCD as screenshot (for debuging)  
  *possible values*: `true` or `false`
* **verbose** - Show more debug logs, be more verbose (for debugging)
  *possible values*: `true` or `false`
* **check_bios** - check for new version of DCS-BIOS during start of DCSpy.  
  *possible values*: `true` or `false`
* **git_bios** - If set to `True` Git/Live version of DCS-BIOS with be used  
  *possible values*: `true` or `false`
* **git_bios_ref** - Git valid reference i.e. branch name, tag, SHA of commit etc.
  *possible values*: any Git valid reference


## Troubleshooting
If you encounter any problem during DCSpy usage, please enable these options:

![image](https://github.com/emcek/dcspy/assets/475312/f7513b0d-f4b5-4a58-a37b-10d9a6f384e6)

Restart DCSpy, try reproduce problem and collect data:

![image](https://github.com/emcek/dcspy/assets/475312/473e4135-59ef-41f1-a895-91284fc6c5b0)
