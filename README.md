# CSGO-autoexec
My personal settings &amp; some recommended sane defaults


### Launch Options
   -language textmodorel -novid -nojoy -nothreadedsockets -softparticlesdefaultoff -tickrate 128


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


[Video Settings](video.txt) - I play at 4:3 Stretched, 1440x1080, fullscreen stretched, with "fancy" detail settings on GTX 1060

Advanced Video | Setting
------------ | -------------
Global Shadow Quality:    |   Medium
Model / Texture Detail   |   High
Texture Streaming   |   Disabled
Effect Detail   |   High
Shader Detail   |   High
Boost Player Contrast   |   Enabled
Multicore Rendering   |   Enabled
Anti-Aliasing   |   4X MSAA
FXAA   |   Disabled
Vertical Sync   |   Disabled
Motion Blur   |   Disabled
Triple-Monitor   |   Disabled
Uber Shaders   |   Enabled
   

### NVIDIA Control Panel Settings

*Good luck changing these if your system language is Finnish* 

Install your NVIDIA GeForce Driver using NVCleanstall. In Expert Settings make sure to Enable MSI-mode & Disable HDCP for lowest input lag, skip GeForce Experience, Telemetry & other bullshit!

Use these settings to minimize input lag and make the game feel more responsive/smooth and reduce microstutters. Import [wgeforce.nip](wgeforce.nip) and apply settings with nvidiaProfileInspector first, after that make your personal adjustments.


#### **Global**

Feature | Setting
------------ | -------------
DSR - Factors   |   Off


#### **Program Settings**

Feature | Setting
------------ | -------------
Ambient Occlusion	|   Off
Antialiasing - Gamma correction |   Off
Low Latency Mode	| Ultra
Power management mode   |   Prefer maximum performance
Preferred refresh rate  |   Highest available
Shader Cache Size    |   Unlimited
Texture filtering - Anistropic sample optimization  |   On
Texture filtering - Negative LOD bias  |   Allow
Texture filtering - Quality  |   High performance
Texture filtering - Trilinear optimization  |   On
Threaded optimization  |   Off
Triple buffering  |   Off
Vertical Sync  |   Off

### csgo.exe Properties
`Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Local Files > Browse Local Files`

Right click csgo.exe and:
`Compatibility > [x] Disable fullscreen optimizations`

`Change high DPI settings> [x] Override high DPI scaling behavior. Scaling performed by: Application`


Use these settings to minimize input lag and make the game feel more responsive/smooth and reduce microstutters.



### Other tweaks?
If you are using Win 10 disable Game Bar, Xbox DVR, Focus Assist and all other annoying FPS-stealing bullshit.
Or just use https://github.com/W4RH4WK/Debloat-Windows-10

#### Disable HDCP
`[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Class\{4d36e968-e325-11ce-bfc1-08002be10318}\0000]`

`"RMHdcpKeyglobZero"=dword:00000001`


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
