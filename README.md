<div align="center">

# 🎮 Game Specific Patches & DLL Wrappers  

***created and maintained by***

[![Chip-Biscuit Website](https://img.shields.io/badge/Chip--Biscuit-Website-blue?style=for-the-badge)](https://chip-biscuit.github.io/)

Reverse Engineering • Programming • Patching • Game Improvements • DLL Creation 

[![Total Downloads](https://img.shields.io/github/downloads/Chip-Biscuit/James-Bond-Quantum-of-Solace-PC-Fix/total?style=flat-square)](https://github.com/Chip-Biscuit/James-Bond-Quantum-of-Solace-PC-Fix/releases/tag/QOS)


<sub>click the Total Downloads button above to take you to the releases page and download the zip at the bottom</sub>

</div>

# James Bond Quantum of Solace PC Fix

This fix is designed with only the Single Player portion of the game in mind. If you wish to play the Multiplayer side, then please go to Plutonium Client where they deal with this side of the game.

![ezgif-2abf7f0f9f74038f](https://github.com/user-attachments/assets/a541c1b1-efdf-43f4-a0ff-023510671990)


# Instructions
Go to release, download the JamesBondQuantumofSolaceFix.zip file and extract it, then put the d3d9.dll and d3d9.ini files into your game folder next to the JB_Launcher_s.exe file. 

You can edit the settings you wish to use in the d3d9.ini file.

# FPS
Default for FPS is 60 which you can change in the d3d9.ini file. The user can use the FPS toggle if they find it breaks at certain points at too high FPS. The toggle will set it back down to the original 30fps. When in game, press the hotkey the user has chosen in [hotkey]keycodes.txt and enter the virtual code in the d3d9.ini to toggle between the original and the new FPS setting.

# FOV
The user has 4 different FOVs to choose from. When in game, press the hotkey the user has chosen in [hotkey]keycodes.txt and enter the virtual code in the d3d9.ini to toggle between the original and the new FOV settings anytime in game.

# Controller
This is the first as accurate as possible implementation of controller support written by Chip (ChipXinput) for the Single Player of this game. The layout is the same as the layout of the Xbox 360 release of the game.

**VERY IMPORTANT – user must go into the games option menu controls and set the ‘Cycle Weapon’ option to ‘5’. If this is not done, then the ability to cycle weapons will not work.**

QTEs (Quick Time Events) will still show up as keyboard prompts so it is advised that the user makes a note of what these keys correspond to on the controller.

you can fully customize the layout of the controller inside of d3d9.ini all explained inside the configuration file.

The default layout is as follows:

<img width="1658" height="1133" alt="Screenshot_2026-01-28_183726" src="https://github.com/user-attachments/assets/152824e9-dff8-47e0-baa2-cc3e75a51643" />

<img width="1427" height="1697" alt="Screenshot_2026-01-28_144241" src="https://github.com/user-attachments/assets/55936bd2-a10b-4fbd-bfb8-24066e4a6ae5" />

you can use controller also for the FOV toggle and FPS toggle by default it would be RB + left FPS toggle, RB + right FOV toggle. if you change the hotkeys for FOV and FPS here: 

        [FOV] 
        hotkey_vk=0x05

        [FPS]
        toggle_vk=0x06 

you will have to update the corresponding key here:

        combo6=RB+DpadRight
        combo6_vks=0x05 ----- FOV toggle <- make sure this matches the same hotkey as under [FOV above]
        combo6_modes=HOLD
        combo6_suppress=1

        combo7=RB+DpadLeft
        combo7_vks=0x06 ----- FPS toggle <- make sure this matches the same hotkey as under [FPS above]
        combo7_modes=HOLD
        combo7_suppress=1

# Mod Menu
This fix includes the mod menu from https://www.speedrun.com/qos/resources/6sb4i for convenience of the end user to have everything all together in one fix and to preserve the menu so that it is not lost. 
**FIX ENHANCERS MAKES IT CLEAR THAT IT DID NOT MAKE THIS MOD MENU AND IF THE ORIGINAL CREATOR WISHES IT REMOVED FROM THE FIX, THEN IT WILL BE REMOVED**.

All this Dll does with mod menu is installs the required file for you via automation instead of having to do it yourself, it will also revert back to the original file if on = 0 under [modmenu] in the ini

The user can turn on the Mod Menu inside of the d3d9.ini file via the option [ModMenu] which is off ‘0’ by default. Once turned on in the d3d9.ini file to activate in-game, press Tab then use the ‘2’ key. Left Click and Right Click to navigate the menus, ‘F’ to select, and ‘Q’ to exit. Note that the first step is always tied to opening the phone and will reflect if this binding is changed from the default Tab.

Vote to see the game return via GOG Dreamlist
If you are interested in potentially seeing this game easily available to purchase and use today then go and vote on the games GOG Dreamlist to help make this become a reality, you can vote for the game here and write a message about the game if you wish – https://www.gog.com/dreamlist/game/james-bond-007-quantum-of-solace-2008 

# Issues/Problems
If you have any issues, with the fixes then please go to discord for help linked below.
https://discord.gg/eVJ7sQH7Cc

# Credits

Credit to Elisha Riedlinger for the base wrapper and ThirteenAG.

Credit to GitHub user "SuperSamus" for pointing out that FPS limit should not be hardcoded to a high limit.

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
