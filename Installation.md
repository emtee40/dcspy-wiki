# Requirements
* [Python 3.11](https://www.python.org/downloads/) but 3.7+ (with tcl/tk support, see installation) should be fine, please choose **Windows x86-64** version, file should be `python-3.11.0-amd64.exe`.  
* [Logitech Gaming Software 9.04.49](https://support.logitech.com/software/lgs)
* [DCS-BIOS 0.7.48](https://github.com/DCSFlightpanels/dcs-bios/releases/latest) or newer (can be installed directly form DCSpy)

**Note if you upgrade from 1.5.1:**
* Older version of DCSpy required Logitech LCD SDK ver. 8.57.148 (`C:\Program Files\Logitech Gaming Software\LCDSDK_8.57.148`). Since DCSpy 1.6.0 use built-in SDK in LGS (Logitech Gaming Software), you can safely remove/delate from your system.

# Installation
There are two ways of install DCSpy: single file download (basic / new way) or via Python package manager (advanced / old way). Both have advantages and  disadvantages. For new users it is recommended to use first one, current users can stick to old way or switch to new way. Both will be supported.

## Single file download (new way)
* Advantage: Simple download and you are ready to go
* Disadvantage: Windows Defender can block download/execution

1. Go to [Releases](https://github.com/emcek/dcspy/releases), from Assets section download one of:
   * `dcspy_*.exe` - simple one window application
   * `dcspy_cli_*.exe` - during start you will see additional console window with logs and more details
2. Place file anywhere in your system, double click to start.
3. DCS-BIOS
   * You can skip for now and install DCS-BIOS directly from Dcspy (Config -> Check DCS-BIOS). Check **dcsbios** config flag before, see [Configuration](usage#configuration).  
     It checks if new version exists, download, and unpack DCS-BIOS to `Save Games` folder and check `Export.lua` file.
   * Or follow manual installation [DCS-BIOS wiki page](https://github.com/DCSFlightpanels/DCSFlightpanels/wiki/Installation)

Due to how Python application can be pack into executable file, Windows Defender can recognize it as a virus. See more details [here](Information#windows-defender)

## via pip (old way)
* Advantage: Better control, simple update process, no Defender hassle
* Disadvantage: More steps, more complicated process

1. Install all requirements
2. During Python installation please select  
   * Optional Features:
     * pip
     * tcl/tk and IDLE
     * py launcher  
   * Advanced Options:
     * Associate files with Python (requires the py launcher)
     * Add Python to environment variables
     * Customize install location: **C:\Python311** or **C:\Python**
3. Logitech Gaming Software installation is straightforward.
4. DCS-BIOS
   * You can skip for now and install DCS-BIOS directly from Dcspy (Config -> Check DCS-BIOS). Check **dcsbios** config flag before, see [Configuration](usage#configuration).  
     It checks if new version exists, download, and unpack DCS-BIOS to `Save Games` folder and check `Export.lua` file.
   * Or follow manual installation [DCS-BIOS wiki page](https://github.com/DCSFlightpanels/DCSFlightpanels/wiki/Installation)
5. Package is available on [PyPI](https://pypi.org/project/dcspy/), open Windows Command Prompt (cmd.exe) and type:
```shell script
pip install dcspy
```
or download manually wheel file from [releases](https://github.com/emcek/dcspy/releases/latest):
```shell script
pip install dcspy-1.7.4-py3-none-any.whl
```
**Note:** If you got `pip is not recognized as an internal or external command, operable program or batch file.` error, see [FAQ](Information#faq)


**Next step:** [Usage](https://github.com/emcek/dcspy/wiki/Usage)
