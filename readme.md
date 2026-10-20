CATEGORICALLY BETTER -- VERSION 0.8.3
==================================
Urbek City Builder | Construction Menu Overhaul

WHAT THIS MOD DOES
------------------
It helps my OCD. 

No, seriously. Have you noticed how a crazy number of city buildings 
incomprehensibly fall under "landmark" instead of commerce, or civic buildings 
or whatever? That's been completely adjusted so that the menu buttons make sense!

So, Categorically Better reorganizes Urbek's construction menus, introduces 
Commerce, Services and Civic Structures tabs, reassigns vanilla buildings to 
sensible categories, and expands the submenu layout. It does not change vanilla 
building costs, benefits requirements, unlocks, and even retains the "landmark" 
category since other mods may use it. (Skyscrapers go here as well.) 

YES YOU CAN USE THIS ON OLD SAVES!! Urbek is cool that way. 

**IMPORTANT: THIS IS A DEEPER MOD THAN A NORMAL URBEK MOD**

So it not enabled through the game's mod menu and it has its own installer. It
applies runtime modifications using BepInEx and Harmony. IT DOES NOT CHANGE THE 
GAME'S ORIGINAL CODE FILES ON DISK, AND IS COMPLETELY REVERSIBLE. So for coders,
The original Urbek.exe, Assembly-CSharp.dll and resources.assets are not replaced. 
Disable the plugin and restart the game to restore vanilla menus.

INSTALLATION -- WINDOWS (64-BIT URBEK)
-------------------------------------
1. EXIT URBEK completely.
2. In explorer, go to the MAIN GAME DIRECTORY that contains Urbek.exe, usually:
      [drive letter]:\SteamLibrary\steamapps\common\Urbek
   Example -- C:\SteamLibrary\steamapps\common\Urbek
3. EXTRACT THIS ENTIRE ZIP INTO THAT DIRECTORY, preserving the ZIP's folder
   structure. Do not extract it into Urbek_Data or StreamingAssets directly.
   This needs and already includes BepInEx 5.4.23.5 x64 FILES (not another ZIP),
   so winhttp.dll and doorstop_config.ini land BESIDE Urbek.exe and
   BepInEx\core is created inside the main game directory.
   IMPORTANT: If BepInEx is already installed, preserve/skip your existing
   files rather than automatically overwriting a different version.
   3a. If you are installing a new version of "Categorically Better" OVER an old
       version, then yes, overwrite the other files when you extract the new zip. 
4. Open CategoricallyBetter.exe in the MAIN Urbek folder,
   next to Urbek.exe, and click INSTALL / REPAIR. The complete manager is in:
      Urbek_Data\StreamingAssets\Categorically Better Mod
   If you want, you can start the manager directly from that folder.
5. Click ENABLE in the Categorically Better manager.
6. Click LAUNCH URBEK. You can also launch through Steam as usual.

Going forward, you can use the .exe or steam to launch as normal. 

PLEASE NOTE: When launched through the installer/manager, Urbek may activate
once briefly and close, then activate again and launch normally. Allow time for
the second Steam launch rather than treating the first close as a failure.

ABOUT THIS INSTALLER
-------------------
- BepInEx is portable and needs correct file placement, NOT a Windows MSI/setup.
- The supplied release includes BepInEx 5.4.23.5 x64, so an Internet connection
  is crazily NOT required just to obtain BepInEx on supported 64-bit installations.
- On Install / Repair, the manager detects existing BepInEx, preserves it when
  it is compatible, compiles the mod plugin automatically against your installed
  Urbek/Unity/BepInEx assemblies, then places it under BepInEx\plugins.
- There is NO command line or manual compilation required for the player.
  This 0.8.1 build still relies on the Windows .NET Framework C# compiler being
  available; the DLL is not yet precompiled in the release archive.
- The manager also installs and verifies the three icon files.
- Older Urbek.MenuReorder installations are migrated by disabling their old
  DLL to avoid conflicting runtime patches; the old files are kept.
- The first installation leaves Categorically Better DISABLED until ENABLE
  is clicked. Repairs preserve the enabled/disabled state.

ENABLE / DISABLE / REMOVE
-------------------------

TO UNINSTALL THIS MOD AND TAKE URBEK BACK TO ITS EARLIER STATE:

Simply open the "CategoricallyBetter" launcher again and hit "disable". 
(I do not have a file cleanup at this time, so you gotta grab those, 
but simply having them in the folder will not affect your game.)

Enable: Activates the plugin on the NEXT Urbek launch.
Disable: Renames the plugin DLL to CategoricallyBetter.dll.disabled. Its menu
         changes disappear on the NEXT Urbek launch with no recompilation needed.
Install / Repair: Reinstalls the mod plugin and bundled icons and does not overwrite
                  your original Urbek executable, assemblies, or saved games.
Update Menu Icons (no build): Refreshes the three icon PNG files with SHA-256
                              verification; restart Urbek to reload their sprites.

To remove Categorically Better entirely, with the game closed, remove only
BepInEx\plugins\CategoricallyBetter and optionally the config file below.
Do NOT delete shared BepInEx files if other plugins rely on them. If you only
want Urbek's original menus, the Disable button is sufficient.


WHAT'S CHANGED EXACTLY?
-----------------------

THE NEBULOUS LANDMARK CATEGORY GOT A TRIM:

12 buildings have moved to a new category called "Commerce"

 Minimarket, local markets, fish market, repair shop, hardware store, supermarket, 
 banks (small and normal), shopping mall, traditional market, bazaar, and free market.

11 buildings have moved to a new category called "Services"

 Police stations and upgrades, fire station, pharmacy, clinic, hospital, 
 psychiatric hospitals and upgrades, and the prison.

9 buildings have moved to a new category called "Civic" 

 Neighborhood council, city council, association, anarchist community, radio stations 
 and upgrades, Ministry of Security, and government palace.

4 buildings have been moved to "Education"
 Food research, energy research, and advanced research facilities.

3 buildings (including an easter egg) have moved to "Housing"

 Occupied mansion, abandoned mansion, and the developer's hidden house.


All icons have been made, positioned, submenus aligned, all working, and all should 
"unlock" at the correct points. 

TROUBLESHOOTING
----------------

1. WHY DOES URBEK SHOW 0xc000007b / BAD IMAGE / FAIL TO START?
This mod uses a Unity loader called BEPINEX, x64 bit version. You may have the 32-bit 
version installed. Though I did bundle BEPINEX to make things easy, THIS DISTRIBUTION 
BUNDLES x64 BEPINEX ONLY. If your Urbek.exe is 32-bit, do not
launch it with this package's x64 winhttp.dll. Get the official x86 5.4.23.5:
https://github.com/BepInEx/BepInEx/releases/download/v5.4.23.5/BepInEx_win_x86_5.4.23.5.zip

For the official x64 release, see:
https://github.com/BepInEx/BepInEx/releases/download/v5.4.23.5/BepInEx_win_x64_5.4.23.5.zip

Before switching architectures: as always, close Urbek, back up the existing BepInEx
loader files, and consult any other plugin requirements. Replace the loader
components with the appropriate official architecture. The installer checks
the loader's architecture against the game and refuses a mismatch. 

2. WHY ARE THE NEW CATEGORY ICONS JANKY?
It's likely the bilinear filtering the game which may be set to off. To 
toggle filtering, close Urbek and edit:
    [Urbek root]\BepInEx\config\local.urbek.categoricallybetter.cfg
And go to the [Icons] section, change the exact line:
    CrispIcons = false
TO:
    CrispIcons = true
Save and restart Urbek. Note that point sampling can introduce a visible
stair-stepped appearance on thin lines. Change back to true if preferred.
If the configuration file does not exist, Enable the mod, run Urbek once,
then exit and check again.

3. HOW CAN I ENABLE THE MOD IN URBEK'S MODS MENU?
You cannot. Categorically Better changes runtime menus through BepInEx/Harmony,
not Urbek's normal mod launcher in game. Run CategoricallyBetter.exe in:
    Urbek_Data\StreamingAssets\Categorically Better Mod
Click Install / Repair, then Enable.

4. WHY DOES THE IN-GAME MENU STILL LOOK THE SAME?
- Ensure you clicked ENABLE; a new installation starts disabled.
- Close/restart Urbek fully to reload the plugin.
-  Check BepInEx\LogOutput.log for loader or plugin errors.
- Confirm the BepInEx folder is in the same DIR as Urbek.exe, 
  NOT in StreamingAssets or anywhere else.
- Confirm there is only one active menu patch plugin. The installer should
  disable a prior Urbek.MenuReorder.dll during migration.

5. WHY DID THE ICONS FAIL TO UPDATE?
- Close Urbek completely; the plugin caches Unity sprites for each session.
- Open the manager and choose Update Menu Icons (no build).
- Make sure the actual destination is:
    [Urbek root]\BepInEx\plugins\CategoricallyBetter\icons\
  with civic.png, commerce.png and services.png directly under this folder.
- The icon updater backs up old files and checks each installed SHA-256 hash.
- Avoid editing a different or older copy of the plugin's icons.

6. WHY DOES INSTALLATION REPORT COMPILER MISSING OR COMPILE FAILURE?
This release compiles CategoricallyBetter.dll on your machine using the Windows
.NET Framework csc.exe compiler, the shipped BepInEx and your installed Urbek
Unity libraries. The installer does not require users to run the compiler
manually. If the build fails, read the manager log for the specific error.
The release does NOT ship a precompiled CategoricallyBetter.dll yet.

7. WHY DOES URBEK BRIEFLY START, CLOSE, THEN START AGAIN?
This can happen when Steam hands off the game's launch process. There will be a
second launch. If Urbek never returns, inspect Steam and BepInEx\LogOutput.log.

8. CAN THIS MOD CHANGE THE ORIGINAL GAME OR DAMAGE SAVES?
The plugin changes in-memory UI behavior. It does not patch Urbek.exe,
Assembly-CSharp.dll, or resources.assets on disk. It does not intentionally
modify saved-city data. Click Disable and restart to go back to the old menus.

9. I INSTALLED A PREVIOUS 'URBEK MENU REORDER' MOD. WHAT DO I DO?
Yes. Install / Repair should disable the old dll and migrate
its configuration when a new Categorically Better plugin is installed.
Don't enable both plugins simultaneously; overlapping Harmony patches can
conflict. Existing icons and old files are retained as a rollback backup.

10. WHY DOES BEPINEX STILL EXIST AFTER I CLICK DISABLE?
Disable affects only CategoricallyBetter.dll. BepInEx is a common loader and
can support other mods. Leave it in place. Removing the CategoricallyBetter
plugin is sufficient to restore vanilla menus.

11. PERMISSION DENIED / MOD MANAGER WON'T LAUNCH
Exit Urbek, check that the ZIP was extracted into the actual Steam game
folder, and verify you can write there. The real executable is at:
    [Urbek root]\Urbek_Data\StreamingAssets\Categorically Better Mod\CategoricallyBetter.exe
If needed, look for the startup log here:
    %TEMP%\CategoricallyBetter_startup_error.log
The game's BepInEx log is:
    [Urbek root]\BepInEx\LogOutput.log


CREDITS AND LICENSES
--------------------
BepInEx and its dependencies are third-party open-source software, redistributed
under their applicable licenses. See ThirdPartyLicenses for notices and LGPL.
Categorically Better is an independent mod, not affiliated with the developers
of Urbek City Builder or BepInEx. No original Urbek binaries are distributed.

CUSTOM CATEGORY TOOLTIP FIX (v0.8.1)
------------------------------------
Commerce, Services and Civic Structures now show native-style hover labels.
The game's translation data does not contain these new category names; this
release supplies them at runtime when the mouse enters a custom category tab.
To apply on an existing installation, close Urbek, launch CategoricallyBetter.exe,
select Install / Repair, and restart the game. An icon-only update will NOT
update tooltip logic; Install / Repair recompiles the updated plugin.
