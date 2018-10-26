# CSGO-autoexec
My personal settings &amp; some recommended sane defaults


### Launch Options
    -language textmodorel -tickrate 128 -novid -nod3d9ex -console +mat_queue_mode 2 +exec autoexec.cfg -nojoy -threads 4

Required for "-language textmodorel": https://gamebanana.com/gamefiles/3711

Change to -tickrate 64 if you want to practice smokes for Valve MM

Enter launch options at
`Steam > Library > Counter-Strike: Global Offensive (right-click) > Properties > Set Launch Options...`



### Config Files

*video.txt and all .cfg files* needs to be put in `...\Steam\userdata\<Steam3 ID>\730\local\cfg`


[buyscript.cfg](buyscript.cfg)


[autoexec.cfg](autoexec.cfg) - Contains all my personal tweaks and some binds.


[autoexec_stripped.cfg](autoexec_stripped.cfg) - Stripped version for a more general "sane defaults"-version, rename to autoexec.cfg


[Video Settings](video.txt) - I play at 1280x960 4:3 Stretched, with "fancy" detail settings on GTX 1060



### NVIDIA Control Panel Settings

*Good luck changing these if your system language is Finnish* 

Run driver 378.49 for most FPS on older CPU's.

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
