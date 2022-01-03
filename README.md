# Final Fantasy VII The Reunion Linux Install Guide

## Steam
  Install FF7 through Steam</br>
  Select proton version in steam</br>
  Run game once through steam to create proton/wine prefix</br>

  protontricks 39140 uninstaller</br>
  click 'install' and run The_Reunion_R06j.exe</br>
  Install to steamapps/common/FINAL FANTASY VII</br>

  protontricks 39140 regedit</br>
  Registry > Import Registry File > ff7_steam.reg</br>

  add steam ff7 launch options:		export WINEDLLOVERRIDES="ddraw=n,b"; %command%
  
## Lutris
  To play through Lutris you need Final Fantasy VII 1.02 Official Patch
  https://community.pcgamingwiki.com/files/file/600-final-fantasy-vii-102-official-patch/
  Make sure to set the DLL override, import the .reg, and run ff7.exe (NOT steam's ff7_en.exe)
