# Final Fantasy VII Reunion Wine Install Guide

Steam
  Install FF7 through Steam
  Select proton version in steam
  Run game once through steam to create proton/wine prefix

  protontricks 39140 uninstaller
  click 'install' and run The_Reunion_R06j.exe
  Install to steamapps/common/FINAL FANTASY VII

  protontricks 39140 regedit
  Registry > Import Registry File > ff7_steam.reg

  add steam ff7 launch options:		export WINEDLLOVERRIDES="ddraw=n,b"; %command%

  To play through Lutris you need Final Fantasy VII 1.02 Official Patch
  https://community.pcgamingwiki.com/files/file/600-final-fantasy-vii-102-official-patch/
  Make sure to set the DLL override, import the .reg, and run ff7.exe (NOT steam's ff7_en.exe)
