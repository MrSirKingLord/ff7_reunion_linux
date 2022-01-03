# Final Fantasy VII The Reunion Linux Install Guide

## Prerequisites
  wine
	lutris (optional)
	steam (optional)
	protontricks (when running through steam)

## Steam / Proton
  Install FF7 through Steam</br>
  Select proton version in steam</br>
  Run game once through steam to create proton/wine prefix</br>

  protontricks 39140 uninstaller</br>
  click 'install' and run The_Reunion_R06j.exe</br>
  Install to steamapps/common/FINAL FANTASY VII</br>

  protontricks 39140 regedit</br>
  Registry > Import Registry File > ff7_steam.reg</br>

  add steam ff7 launch options:		export WINEDLLOVERRIDES="ddraw=n,b"; %command%
  
## Lutris / Wine
  To play through Lutris you need Final Fantasy VII 1.02 Official Patch</br>
  https://community.pcgamingwiki.com/files/file/600-final-fantasy-vii-102-official-patch/</br>
  Make sure to set the DLL override, import the .reg, and run ff7.exe (NOT steam's ff7_en.exe)</br>
  
## Wine
