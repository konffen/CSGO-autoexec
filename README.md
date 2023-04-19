# CSGO-autoexec
My personal settings &amp; some recommended sane defaults


### Launch Options
`-language textmodorel -novid -nojoy -nothreadedsockets -softparticlesdefaultoff -tickrate 128`


Enter launch options into the box here:

`Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Launch Options`

Required for "-language textmodorel":
Put  [csgo_textmodorel.txt](csgo_textmodorel.txt) in 'csgo/resource' folder.

Change to `-tickrate 64` if you want to practice smokes for Valve MM

Add `-allow_third_party_software` if you want to use Game Capture in OBS Studio (won't allow you to play trusted MM)



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


### Ingame Video Settings
[Video Settings](video.txt) - I play at 4:3 Stretched, 1440x1080, fullscreen stretched, with "fancy" detail settings on GTX 1060, these should give you the biggest visual advantage with least amount of fps lost. Benchmark reference: https://www.youtube.com/watch?v=e2e26BGdPxk

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

Install your NVIDIA GeForce Driver using [NVCleanstall](https://www.techpowerup.com/download/techpowerup-nvcleanstall/). Under `[x] Show Expert Tweaks` select `[x] Enable Message Signaled Interrupts` & `[x] Disable HDCP` for lowest input lag, skip GeForce Experience, Telemetry & other bullshit!

Use these settings to minimize input lag and make the game feel more responsive/smooth and reduce microstutters. Import [wgeforce.nip](wgeforce.nip) and apply settings with [nvidiaProfileInspector](https://github.com/Orbmu2k/nvidiaProfileInspector) first, after that make your personal adjustments.


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
Regedit key below for manual edit, not needed if you install with NVCleanstall and tick `[x] Disable HDCP` under Expert Tweaks

`[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Class\{4d36e968-e325-11ce-bfc1-08002be10318}\0000]`

`"RMHdcpKeyglobZero"=dword:00000001`


### Control flow guard
Disables Windows Defender from scanning through game files...
`Win -> Exploit protection (System settings) -> Program settings -> + Add program to customize -> Choose exact file path -> Browse to csgo.exe -> Control flow guard (CFG) -> [x] Override system settings -> Off -> Apply!`


#### HPET
HPET has changed in newer Windows 10 releases, also some BIOS/UEFI force it on, some have a option for it, different results between Intel/AMD CPUs... your results may vary, don't touch or test both options.


Old tweak method: Run CMD as Admin:

```bcdedit /deletevalue useplatformclock

bcdedit /set useplatformtick yes

bcdedit /set disabledynamictick yes´´´



New tweak method: Run CMD as Admin:

```bcdedit /set nx optout

bcdedit /deletevalue useplatformtick

bcdedit /deletevalue useplatformclock

bcdedit /set disabledynamictick yes´´´



Reboot after!

Use Intelligent standby list cleaner (ISLC) to force 0.50 ms timer:
https://www.wagnardsoft.com/ISLC/ISLC%20v1.0.2.2.exe

#### Check for latency issues
http://www.resplendence.com/latencymon
