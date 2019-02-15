# CSGO-autoexec
My personal settings &amp; some recommended sane defaults


### Launch Options
    -language textmodorel -tickrate 128 -novid +exec autoexec.cfg -nojoy

### Launch Options (old, Valve says "use less or none" so trying the above for now)
    -language textmodorel -tickrate 128 -novid -nod3d9ex -console +mat_queue_mode 2 +exec autoexec.cfg -nojoy -threads 4


Required for "-language textmodorel": https://gamebanana.com/gamefiles/3711

Change to -tickrate 64 if you want to practice smokes for Valve MM

Enter launch options at
`Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Set Launch Options...`



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

Run NVIDIA GeForce Driver Version: 378.49 for most FPS on older CPU's. Version 387.92 also seems to be recommended. 

Use these settings to minimize input lag and make the game feel more responsive/smooth and reduce microstutters.

#### **Global**

Feature | Setting
------------ | -------------
DSR - Factors   |   Off


#### **Program Settings**

csgo.exe

Feature | Setting
------------ | -------------
Ambient Occlusion	|   Off
Antialiasing - Gamma correction |   Off
Maximum pre-rendered frames	| 1
Power management mode   |   Prefer maximum performance
Preferred refresh rate  |   Highest available
Shader Cache    |   Off
Texture filtering - Anistropic sample optimization  |   On
Texture filtering - Negative LOD bias  |   Clamp
Texture filtering - Quality  |   High performance
Texture filtering - Trilinear optimization  |   On
Threaded optimization  |   On
Triple buffering  |   Off
Vertical Sync  |   Off
Virtual Reality pre-rendered frames  |   1

### NVIDIA Profile Inspector
Download: https://www.guru3d.com/files-details/nvidia-inspector-download.html

Use these settings to minimize input lag and make the game feel more responsive/smooth and reduce microstutters.

**Profiles:** *Counter-strike: Global Offensive*

Feature | Setting
------------ | -------------
Frame Rate Limiter 2 Control | 0x00000004 PS_FRAMERATE_LIMITER_2_CONTROL_DELAY_FLIP_BY_FLIPMETERING

### Other tweaks?
If you are using Win 10 disable Game Bar, Xbox DVR, Focus Assist and all other annoying FPS-stealing bullshit.
Or just use https://github.com/W4RH4WK/Debloat-Windows-10

#### HPET
Try to Enable/Disable HPET in BIOS/UEFI.

Related tools:
https://vvvv.org/contribution/windows-system-timer-tool

#### Check for latency issues
http://www.resplendence.com/latencymon
