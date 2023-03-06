# HogwartsLegacyPerformanceFix
Hogwarts Legacy currently has many technical issues causing degraded performance and stuttering; especially if you want to use high end features such as Ray Tracing. I have created this guide with a list of optimizations that has greatly improved my performance using Ray Tracing and High settings. RTX 3080 + Ryzen 5800x.

Disclaimer: There are several different issues to resolve with the game. So each one has its own unique impact on performance. This is not a one size fits all solution and I recommend using each step and determing which are necessary for your specific game performance; though the DLSS update is the exception and anyone looking to improve overall game performance should do it.

(Update DLSS Version - MOST IMPORTANT)
For some reason, the base game comes with a very outdated DLSS version 2.3.11 (Current version 3.1.1). Free performance with an DLSS version update:

URL: https://www.techpowerup.com/download/nvidia-dlss-dll/

Guide: Paste downloaded "nvngx_dlss.dll" in "Hogwarts Legacy\Engine\Plugins\Runtime\Nvidia\DLSS\Binaries\ThirdParty\Win64" Overwrite files when prompted to do so.

(MOD) (SLPF - Stuttering and Low Performance Fix) Hogwart's has an issue where high end features such as Raytracing cause severe stuttering issues. This Mod greatly assists in reducing the massive FPS spike decrease when the stutter occurs.
(I included this in the GitHub repo) URL:https://www.nexusmods.com/hogwartslegacy/mods/120

Guide: Navigate to "/Phoenix/Plugins/ChromaSDKPlugin/Binaries/Win64" and renamed the file "CChromaEditorLibrary64.dll" to "Original.dll" or back it up to another location. Paste "CChromaEditorLibrary64.dll" from the "Mods/SLPF 120-1-5-1677166181/" included in this GitHub repo to you game directory "/Phoenix/Plugins/ChromaSDKPlugin/Binaries/Win64". Overwrite files when prompted to do so.

(Memory Leak issue)
Hogwarts Legacy has memory leak issues (the game fails to release memory when it no longer needs it). For some additional help with stuttering, I have included the extremely simple Reduce Memory application. When configured it will auto optimize memory usage at a specific threshold you set and not allow it to pile up and cause performance issues.

(I included this in the GitHub repo) URL: https://steamcommunity.com/linkfilter/?url=https://www.sordum.org/9197/reduce-memory-v1-6/

Guide: Launch "ReduceMemory_x64" from the "Reduce Memory" directory I included in the GitHub repo. Navigate to "options". Set a limit to automatically optimize memory. Set the limit to 70%. If your system has low memory available and uses 70% memory usage by default, up it to 80%. Set the update interval to 5 seconds.

Note: You'll need to launch this application every time you start your game.

(GPU Control Panel Settings - Unlock your max frame rate in-game)
The game looses a few frames if you set the FPS rate in the game settings for some reason. For example, mine is set to 144 in game and these Nvidia GPU settings gain me a few additional FPS overall. This guide is made for Nvidia users, you'll have to Google how to apply these changes on an AMD GPU.

Guide: Disable V-Sync in-game. Navigate to your GPU control panel -> Manage 3D Settings -> program settings -> add Hogwarts Legacy if it's not already added. Set - Anisotropic Filtering: 8x. Set - Power Management mode: prefer maximum performance.

(Forced Fullscreen Exclusive)
Guide: Navigate to "AppData\Local\Hogwarts Legacy\Saved\Config\WindowsNoEditor" and open "GameUserSettings.ini" in NotePad. Locate these two parameters "FullscreenMode=1" and "LastConfirmedFullscreenMode=1" and set both to zero. Below both lines create a new line "PreferredFullscreenMode=0" without quotation marks, save the file. Set - Vsync: Fast in Nvidia controls settings for HogwartsLegacy.exe if you have not already. Right Click "HogwartsLegacy.exe". Navigate to the Compatibility tab. Check "Disable fullscreen optimizations" and click Apply. HogwartsLegacy.exe ("Hogwarts Legacy\Hogwarts Legacy.exe")

(Possible Future Mods)

Ascendio II.I - FPS Hotfix and Engine Tweaks for Hogwarts Legacy - https://www.nexusmods.com/hogwartslegacy/mods/69?tab=description
