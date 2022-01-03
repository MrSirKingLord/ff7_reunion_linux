# Final Fantasy VII The Reunion Linux Install Guide

These instructions are for the Steam version of FF7. Unfortunately, a legitimate Steam install of FF7 with Proton does not create the necessary registry entries in the wine/proton prefix which The Reunion requires. There is also a wine DLL override necessary for The Reunion to load at all.

If you have the original CDs, there is a video guide here: https://www.youtube.com/watch?v=3nlpvEVLR_s </br>
The installer on the original CDs will give you the necessary registry entries, as will installing through Steam on Windows. I have exported the registry entries to .reg files here for your convenience. They are simple registry entries recording the existence of an installed program like any other, and are in no way malicious or illegal.

## Essentials

wine</br>
winetricks</br>
steam + proton</br>
protontricks</br>
lutris (optional)</br>
[Final Fantasy VII 1.02 Official Patch](https://community.pcgamingwiki.com/files/file/600-final-fantasy-vii-102-official-patch/) (non-steam only)</br>
[The Reunion](https://ff7.live/index.html)</br>
	
## Instructions

### Steam / Proton

#### 1. Install FF7 through Steam</br>

- Select FF7 proton version in steam</br>
- Download and install FF7
- Run game once through steam to create proton/wine prefix, and to ensure game is working</br>

#### 2. Install Reunion with protontricks

`protontricks 39140 uninstaller`</br>

- Click 'install', browse to and run The_Reunion_R06j.exe (or newer version)</br>
- Browse and install to `Z:/home/user/.steam/steam/steamapps/common/FINAL FANTASY VII/`</br>

#### 3. Install the registry entries necessary for The Reunion to run

`protontricks 39140 regedit`</br>

- Registry > Import Registry File > ff7_steam.reg</br>

#### 4. Add wine DLL override necessary for The Reunion to run

- Add Steam FF7 launch options: `export WINEDLLOVERRIDES="ddraw=n,b"; %command%`

### Lutris / Wine

#### 1. Install FF7 through Steam</br>

- Select FF7 proton version in steam</br>
- Download and install FF7

#### 2. Install Final Fantasy VII 1.02 Official Patch</br>

- Copy ff7.exe and FF7Config.exe to `~/.steam/steam/steamapps/common/FINAL FANTASY VII/`</br>

#### 3. Add FF7 to Lutris with DLL override and registry entries

- Add a new game</br>
- Game info</br>
Name: FINAL FANTASY VII</br>
- Game options</br>
Runner: Wine</br>
Executable: `~/.steam/steam/steamapps/common/FINAL FANTASY VII/ff7.exe` (NOT steam's ff7_en.exe)</br>
Wine prefix: `~/.local/share/wineprefixes/ff7` </br>
- Runner options</br>
Wine version: System </br>
DLL Overrides </br>
key: `ddraw`</br>
value: `n,b`</br>
- FINAL FANTASY VII > Wine button > Wine registry</br>
Registry > Import Registry File > ff7_steam.reg</br>

#### 4. Install The Reunion with Lutris

- FINAL FANTASY VII > Wine button > Run EXE inside Wine prefix</br>
Browse to and run The_Reunion_R06j.exe (or newer version)</br>
Browse and install to `Z:/home/user/.steam/steam/steamapps/common/FINAL FANTASY VII/`</br>
  
### CLI / Wine

#### 1. Install FF7 through Steam</br>

- Select FF7 proton version in steam</br>
- Download and install FF7

#### 2. Install Final Fantasy VII 1.02 Official Patch</br>

- Copy ff7.exe and FF7Config.exe to `~/.steam/steam/steamapps/common/FINAL FANTASY VII/`</br>

#### 3. Install the Reunion
`export WINEPREFIX="~/.local/share/wineprefixes/ff7"`</br>
`wine uninstaller`</br>
click 'install', browse to and run The_Reunion_R06j.exe</br>
Browse and install to `Z:/home/user/.steam/steam/steamapps/common/FINAL FANTASY VII/`</br>

#### 4. Install the registry entries necessary for The Reunion to run
`export WINEPREFIX="~/.local/share/wineprefixes/ff7"`</br>
`wine regedit`</br>
Registry > Import Registry File > ff7_steam.reg</br>

#### 5. Add wine DLL override necessary for The Reunion to run, and play.
`export WINEPREFIX="~/.local/share/wineprefixes/ff7"`</br>
`export WINEDLLOVERRIDES="ddraw=n,b"`</br>
`wine ~/.steam/steam/steamapps/common/FINAL FANTASY VII/ff7.exe`</br>

## Playing

- Please read The_Reunion/The Reunion - Help.rtf</br>
- Make sure to edit The_Reunion/Options.ini to your preference</br>
- You should be able to skip cutscenes with `Backspace + L`, if so then The Reunion is working</br>

## Troubleshooting

- Use winehq-stable or winehq-staging instead of wine from your distro, or use wine-staging-tkg or proton-ge
- Steam: delete the proton prefix at `~/.steam/steam/steamapps/compatdata/39140` and try again
- Lutris/CLI: delete the wine prefix at `~/.local/share/wineprefixes/ff7` and try again
