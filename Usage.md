## Usage
1. Run Logitech Gaming Software (it allows updating LCD)
2. You can check with `pip uninstall dcspy` (**NOTE!** answer **No** to question) where dcspy was installed. Usually pip should install dcspy into your python directory: i.e.:
   * `c:\python310\lib\site-packages\dcspy-1.7.0.dist-info\*`
   * `c:\python310\lib\site-packages\dcspy\*`
   * `c:\python310\scripts\dcspy.exe`
3. You can drag and drop `dcspy.exe` to desktop and make shortcut (with custom icon, you can find icon in installation directory i.e. `c:\python310\lib\site-packages\dcspy\dcspy.ico`).
4. Double-click on dcspy icon or type `dcspy.exe` from Command Prompt
5. LCD should update with dcspy basic info, waiting to connect to DCS 
6. Run DCS and start any mission.

**Note:** If you upgrade DCSpy before version 1.7.0 `dcspy.ico` and `config.yaml` were in data directory like `c:\python310\dcspy_data\` but location is deperched in Python if you still have it, you can safely delete it

## Mono vs. Color
DCSpy do not use full potential of G19, which support full RGBA, 8-lines LCD with 7 programmable buttons. In contrast to 
mono devices (like G13, G15 and G510), which support mono, 4-lines LCD with only 4 buttons. Right now DCSpy use only top 
4 lines of LCD and 4 buttons. Way in which actions assign to button for G13 (4 buttons form left to right) are mapped to G19 looks:
* G13 1st button -> G19 left button
* G13 2nd button -> G19 right button
* G13 3rd button -> G19 down button
* G13 4th button -> G19 up button

Maybe in future when settings via config file will be added, then it allowed usage all 7 buttons in G19. But right now 
actions for supported airplanes are hardcoded right now.