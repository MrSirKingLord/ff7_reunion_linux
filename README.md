# Final Fantasy VII The Reunion Linux Install Guide

These instructions are for the Steam version of FF7. Unfortunately, a legitimate Steam install of FF7 with Proton does not create the necessary registry entries in the wine/proton prefix which The Reunion requires. There is also a wine DLL override necessary for The Reunion to load at all.

If you have the original CDs, there is a video guide here: https://www.youtube.com/watch?v=3nlpvEVLR_s </br>
The installer on the original CDs will give you the necessary registry entries, as will installing through Steam on Windows. I have exported the registry entries to .reg files here for your convenience. They are simple registry entries recording the existence of an installed program like any other, and are in no way malicious or illegal.

## Prerequisites

winehq-stable or winehq-staging</br>
winetricks</br>
steam + proton</br>
protontricks</br>
lutris (optional)</br>
Final Fantasy VII 1.02 Official Patch (non-steam only)</br>
The Reunion</br>
	
## Instructions

### Steam / Proton

Install FF7 through Steam</br>
Select proton version in steam</br>
Run game once through steam to create proton/wine prefix</br>

protontricks 39140 uninstaller</br>
click 'install', browse to and run The_Reunion_R06j.exe</br>
Install to steamapps/common/FINAL FANTASY VII</br>

protontricks 39140 regedit</br>
Registry > Import Registry File > ff7_steam.reg</br>

add steam ff7 launch options: export WINEDLLOVERRIDES="ddraw=n,b"; %command%
  
### Lutris / Wine
Install FF7 through Steam</br>
Install Final Fantasy VII 1.02 Official Patch</br>
Make sure to set the DLL override, import the .reg, and run ff7.exe (NOT steam's ff7_en.exe)</br>
  
### CLI / Wine
Install FF7 through Steam</br>
Install Final Fantasy VII 1.02 Official Patch</br>

wine uninstaller</br>
click 'install', browse to and run The_Reunion_R06j.exe</br>
Install to steamapps/common/FINAL FANTASY VII</br>

wine regedit</br>
Registry > Import Registry File > ff7_nonsteam.reg</br>

export WINEDLLOVERRIDES="ddraw=n,b"</br>
wine ff7.exe</br>
