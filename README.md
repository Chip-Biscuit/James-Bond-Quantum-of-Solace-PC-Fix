[![Controller](https://img.shields.io/badge/Controller-XInput%20Support-007ec6?style=flat-square)](#controller)
[![FOV](https://img.shields.io/badge/FOV-Toggle-f39c12?style=flat-square)](#fov)
[![FPS](https://img.shields.io/badge/FPS-Adjustable-2ea44f?style=flat-square)](#fps)
[![Mod%20Menu](https://img.shields.io/badge/Mod%20Menu-INI-8e44ad?style=flat-square)](#mod-menu)
[![Window%20Mode](https://img.shields.io/badge/Window%20Mode-INI-555555?style=flat-square)](#window-mode)



<div align="center">

# 🎮 Game Specific Patches & DLL Wrappers  

***created and maintained by***

[![Chip-Biscuit Website](https://img.shields.io/badge/Chip--Biscuit-Website-blue?style=for-the-badge)](https://chip-biscuit.github.io/)

Reverse Engineering • Programming • Patching • Game Improvements • DLL Creation 

[![Total Downloads](https://img.shields.io/github/downloads/Chip-Biscuit/James-Bond-Quantum-of-Solace-PC-Fix-Controller-Support/QOSUpdate/total?label=Total%20Downloads)](https://github.com/Chip-Biscuit/James-Bond-Quantum-of-Solace-PC-Fix-Controller-Support/releases/tag/QOSUpdate)


<sub>click the Total Downloads button above to take you to the releases page and download the zip at the bottom</sub>

</div>

# James Bond Quantum of Solace PC Fix

This fix is designed with only the Single Player portion of the game in mind. If you wish to play the Multiplayer side, then please go to Plutonium Client where they deal with this side of the game.

![ezgif-2abf7f0f9f74038f](https://github.com/user-attachments/assets/a541c1b1-efdf-43f4-a0ff-023510671990)


# Instructions

Go to [release](https://github.com/Chip-Biscuit/James-Bond-Quantum-of-Solace-PC-Fix-Controller-Support/releases/tag/QOS) and download either:

**[JamesBondQuantumofSolaceFix.zip](https://github.com/Chip-Biscuit/James-Bond-Quantum-of-Solace-PC-Fix-Controller-Support/releases/download/QOSUpdate/JamesBondQOSFix.zip)**  
(d3d9 wrapper) — designed for standard users who just wish to use the fix stand-alone. Simply drag and drop the files into the game folder and launch the game.

or

**[JamesBondQOSFixASI.zip](https://github.com/Chip-Biscuit/James-Bond-Quantum-of-Solace-PC-Fix-Controller-Support/releases/download/QOSUpdate/JamesBondQOSFixASI.zip)**  
(stand-alone DLL provided as Chip.asi) which uses 13AG Ultimate ASI Loader (winmm.dll). This version is intended for users who wish to use the fix in tandem with other DLLs or wrappers.

If the included winmm.dll is not working as intended, you can use any of the alternative loader DLLs from  
[13AG Ultimate ASI Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases). Visit that page for more information on how to use the different loader variants.

winmm.dll loads the files inside the “scripts” folder. Any DLL placed in this folder and renamed from .dll to .asi will be injected into the game.

This version is designed for more advanced users or those wishing to load additional DLL fixes, mods, or wrappers.

---

Extract whichever version you choose (JamesBondQOSFix.zip or JamesBondQOSFixASI.zip), then place the files into your game folder next to JB_Launcher_s.exe.

It is also possible to take Chip.asi and rename it to Chip.dll, then inject it manually using any method you prefer. Make sure chip.ini is placed next to Chip.dll.

**For standard users it is highly recommended to use JamesBondQuantumofSolaceFix.zip (d3d9 wrapper).**

You can edit the settings for JamesBondQuantumofSolaceFix.zip in the d3d9.ini file.  
For JamesBondQOSFixASI.zip, edit settings in: scripts → chip.ini

# Xliveless

This game relies on Games for Windows Live (GFWL), which no longer works reliably on modern versions of Windows.

To avoid launch and save issues, it is recommended to use Xliveless instead:
https://community.pcgamingwiki.com/files/file/576-xliveless/

Xliveless removes the GFWL dependency and allows the game to run normally on modern systems.

# FPS

Default for FPS is 120 which you can change in the d3d9.ini or chip.ini file. The user can use the FPS toggle if they find it breaks at certain points at too high FPS. The toggle will set it back down to the original 30fps. When in game, press the hotkey the user has chosen in [hotkey]keycodes.txt and enter the virtual code in the d3d9.ini or chip.ini to toggle between the original and the new FPS setting.

# FOV Settings

Default is `FOVAutomatic=1`

You can set your preferred in-game FOV using:


         [FOV]
         value=100    ; set this to any FOV you prefer


#### Automatic FOV Mode (FOVAutomatic=1)

If `FOVAutomatic=1`, the game will **always enforce** the FOV from `value=` for the entire session (no hotkey toggle).


         [FOV]
         FOVAutomatic=1
         value=100


#### Toggle FOV Mode (FOVAutomatic=0)

If `FOVAutomatic=0`, the mod enables the **FOV toggle hotkey**. While in-game, press the hotkey configured in `d3d9.ini` or `chip.ini` to toggle between:

- The game’s **original FOV**
- Your **user-defined FOV** (`value=`)


         [FOV]
         FOVAutomatic=0
         value=100


The original FOV is automatically detected and stored when the game initializes, allowing safe switching between the default value and your custom value during gameplay.


# Controller

This is the first as accurate as possible implementation of controller support written by Chip (ChipXinput) for the Single Player of this game. The layout is the same as the layout of the Xbox 360 release of the game.

**VERY IMPORTANT – user must go into the games option menu controls and set the ‘Cycle Weapon’ option to ‘5’. If this is not done, then the ability to cycle weapons will not work.**

QTEs (Quick Time Events) will still show up as keyboard prompts so it is advised that the user makes a note of what these keys correspond to on the controller.

you can fully customize the layout of the controller inside of d3d9.ini all explained inside the configuration file.

**Recomended if you are using the controller to go into the game options -> gameplay -> look sensitivity and turn it down to somewhere between 0 - 4 otherwise it is very fast trying to look around on controller.**

The default layout is as follows:

<img width="1658" height="1133" alt="Screenshot_2026-01-28_183726" src="https://github.com/user-attachments/assets/152824e9-dff8-47e0-baa2-cc3e75a51643" />

<img width="1427" height="1697" alt="Screenshot_2026-01-28_144241" src="https://github.com/user-attachments/assets/55936bd2-a10b-4fbd-bfb8-24066e4a6ae5" />

you can use controller also for the FOV toggle and FPS toggle by default it would be LB + left FPS toggle, LB + right FOV toggle. if you change the hotkeys for FOV and FPS here: 

        [FOV] 
        hotkey_vk=0x05

        [FPS]
        toggle_vk=0x06 

you will have to update the corresponding key here:

        combo6=LB+DpadRight
        combo6_vks=0x05 ----- FOV toggle <- make sure this matches the same hotkey as under [FOV above]
        combo6_modes=HOLD
        combo6_suppress=1

        combo7=LB+DpadLeft
        combo7_vks=0x06 ----- FPS toggle <- make sure this matches the same hotkey as under [FPS above]
        combo7_modes=HOLD
        combo7_suppress=1

you can use controller also for the MOD menu as follows: 

          xbox input ----------------------- keyboard input  ------------------ action
          Select -------------------------------- tab---------------------- open phone menu
          LB + UP -------------------------------- 2----------------------- start the mod menu
          Start --------------------------------- esc --------------------- back to game 
          Right trigger/ Left Trigger --------- rmb/lmb ---------------  navigate the mod menu
          X -------------------------------------- F ------------------- Select things in the menu 
          LB + Down ------------------------------ Q ---------------------- Quit the menu

# Mod Menu
This fix includes the mod menu from https://www.speedrun.com/qos/resources/6sb4i for convenience of the end user to have everything all together in one fix and to preserve the menu so that it is not lost. 
**FIX ENHANCERS MAKES IT CLEAR THAT IT DID NOT MAKE THIS MOD MENU AND IF THE ORIGINAL CREATOR WISHES IT REMOVED FROM THE FIX, THEN IT WILL BE REMOVED**.

All this Dll does with mod menu is installs the required file for you via automation instead of having to do it yourself, it will also revert back to the original file if on = 0 under [modmenu] in the ini

The user can turn on the Mod Menu inside of the d3d9.ini file via the option [ModMenu] which is off ‘0’ by default. Once turned on in the d3d9.ini file to activate in-game, press Tab then use the ‘2’ key. Left Click and Right Click to navigate the menus, ‘F’ to select, and ‘Q’ to exit. Note that the first step is always tied to opening the phone and will reflect if this binding is changed from the default Tab.

you can use controller also for the MOD menu as follows: 

          xbox input ----------------------- keyboard input  ------------------ action
          Select -------------------------------- tab---------------------- open phone menu
          LB + UP -------------------------------- 2----------------------- start the mod menu
          Start --------------------------------- esc --------------------- back to game 
          Right trigger/ Left Trigger --------- rmb/lmb ---------------  navigate the mod menu
          X -------------------------------------- F ------------------- Select things in the menu 
          LB + Down ------------------------------ Q ---------------------- Quit the menu

**important** 

If [modmenu]  on = 1 you are unable to use previous saves but if [modmenu] on = 0 previous saves work just fine make sure if you will be enabling the mod menu to back up any saves you have before use. 

# Vote to see the game return via GOG Dreamlist
If you are interested in potentially seeing this game easily available to purchase and use today then go and vote on the games GOG Dreamlist to help make this become a reality, you can vote for the game here and write a message about the game if you wish – https://www.gog.com/dreamlist/game/james-bond-007-quantum-of-solace-2008 

# Issues/Problems
If you have any issues, with the fixes then please go to discord for help linked below.
https://discord.gg/eVJ7sQH7Cc

# Credits

Credit to Elisha Riedlinger for the base wrapper (d3d9) and ThirteenAG for the ultimate asi loader xlive.dll used in JamesBondQOSFixASI.zip

---

### Fix Enhancers  
https://fixenhancers.wixsite.com/fix-enhancers

“Creating compatibility fixes and enhancements for legacy PC games.”

# Chip
- founder
- reverse engineer
- programmer
- developer
- Game Preservationist
  
<img width="250" height="500" alt="my logoo" src="https://github.com/user-attachments/assets/9bb13d3f-0734-4f1d-b68f-14114b13744a" />


# JokerAlex21 
- founder
- admin
- tester 

<img width="250" height="250" alt="YouTube_Logo" src="https://github.com/user-attachments/assets/5c7204ca-4bca-4673-8117-965732e7ee6d" />
