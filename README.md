# CSGO-autoexec
My personal settings &amp; some recommended sane defaults


### Launch Options
    -language textmodorel -tickrate 128 -novid +exec autoexec.cfg -nojoy


Required for "-language textmodorel": https://gamebanana.com/gamefiles/3711

Change to -tickrate 64 if you want to practice smokes for Valve MM

Enter launch options at
`Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Set Launch Options...`

FINALLY we can Alt+Tab fast!
`– Added an optional -d3d9ex command line switch to reduce CPU memory use by about 40%.`


### Config Files

*video.txt and all .cfg files* needs to be put in `...\Steam\userdata\<Steam3 ID>\730\local\cfg`


[buyscript.cfg](buyscript.cfg)


[autoexec.cfg](autoexec.cfg) - Contains all my personal tweaks and some binds. WARNING: contains:
-CUSTOM CROSSHAIR
-CUSTOM VIEWMODEL
-CUSTOM SOUND SETTINGS FOR 4:3 FOV
-CUSTOM SCOREBOARD BIND WITH NETGRAPH TOGGLE

Remove those parts or use autoexec_stripped.cfg!


[autoexec_stripped.cfg](autoexec_stripped.cfg) - Stripped version for a more general "sane defaults"-version, rename to autoexec.cfg


[Video Settings](video.txt) - I play at 1280x960 4:3 Stretched, with "fancy" detail settings on GTX 1060



### NVIDIA Control Panel Settings

*Good luck changing these if your system language is Finnish* 

Run NVIDIA GeForce Driver Version: 441.41
Debloated by FR33THY, no GeForce Experience, no Telemetry no bullshit!
https://drive.google.com/open?id=1o6VsqHr_Eo09V849a8UXUK37IAv8sieW

Use these settings to minimize input lag and make the game feel more responsive/smooth and reduce microstutters.

#### **Global**

Feature | Setting
------------ | -------------
DSR - Factors   |   Off


#### **Program Settings**
`Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Local Files > Browse Local Files`

Right click csgo.exe and:
`Compatibility > [x] Disable fullscreen optimizations`

Feature | Setting
------------ | -------------
Ambient Occlusion	|   Off
Antialiasing - Gamma correction |   Off
Low Latency Mode	| On
Power management mode   |   Prefer maximum performance
Preferred refresh rate  |   Highest available
Shader Cache    |   Off
Texture filtering - Anistropic sample optimization  |   On
Texture filtering - Negative LOD bias  |   Allow
Texture filtering - Quality  |   High performance
Texture filtering - Trilinear optimization  |   On
Threaded optimization  |   Auto
Triple buffering  |   Off
Vertical Sync  |   Off
Virtual Reality pre-rendered frames  |   1

### csgo.exe Properties
Download: https://github.com/Orbmu2k/nvidiaProfileInspector/releases

Use these settings to minimize input lag and make the game feel more responsive/smooth and reduce microstutters.



### Other tweaks?
If you are using Win 10 disable Game Bar, Xbox DVR, Focus Assist and all other annoying FPS-stealing bullshit.
Or just use https://github.com/W4RH4WK/Debloat-Windows-10

#### HPET
Disable HPET in Windows! Run CMD as Admin:
bcdedit /deletevalue useplatformclock
bcdedit /set useplatformtick yes
bcdedit /set disabledynamictick yes

Reboot after!

Use Intelligent standby list cleaner (ISLC) to force 0.50 ms timer:
https://www.wagnardsoft.com/ISLC/ISLC%20v1.0.2.2.exe

#### Check for latency issues
http://www.resplendence.com/latencymon
