# Thinkpad Hotkey Fix

## Problem Description
See the original issue: [Remapping call keys (F9, F10, F11)](https://www.reddit.com/r/thinkpad/comments/r18cbr/remapping_call_keys_f9_f10_f11/)

Kudos to [csavalas](https://github.com/csavalas), who came up with the initial fix! This is a modified version of his original work.

**New project by csvalas:** https://github.com/csavalas/HotkeyMapper

## Overview
This fix will replace the default actions of the F9 (messages), F10 (answer call) and F11 (hang up call) keys on modern ThinkPads with the following:
```
| Key | New Function |
|-----|-------------|
| F9  | Play/Pause  |
| F10 | Previous song |
| F11 | Next song   |
```
## Requirements
* OS: Windows (tested on 10 & 11)
* Have the [Lenovo Vantage](https://apps.microsoft.com/detail/9wzdncrfj4mv) app installed

## Installation Instructions
1. Download the [latest release](https://github.com/OhShoot01/ThinkPad-Hotkey-Fix/releases/) and extract the `.zip` file to a folder (NOTE: the folder name should **not** contain spaces.)
2. Copy the path of each `ex_9x.vbs` file (*Ctrl + Shift + C* or Right click > Copy as path)
3. Open `tp-hotkeys-fix.reg` with notepad.
4. Replace the paths for each file accordingly (lines `8`, `15` and `22`). 
   * **Do not remove quotation marks from the original file.**
   * You must also replace `\` in the file paths with `\\`
   * Example: `C:\Users\Oh_Shoot01\hotkeys-fix\ex_98.vbs` would become `C:\\Users\\Oh_Shoot01\\hotkeys-fix\\ex_98.vbs`.
5. **If Microsoft Teams is installed on your computer,** delete the last line of code:  `[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\Teams]` 
6. Save and exit the file.
7. Double click the `tp-hotkeys-fix.reg` file.
8. Select Yes/OK on any confirmation dialogs that appear.
9. Done!

**Extra Tip:** If you wish to hide this folder, you can set it to hidden in its properties menu (select *Apply changes to this folder only* if prompted with a Confirm Attribute Changes dialogue).

## Technical Reference
The registry file creates/modifies the following keys:
   * `HKEY_LOCAL_MACHINE\SOFTWARE\Lenovo\ShortcutKey\AppLaunch\Ex_96`
   * `HKEY_LOCAL_MACHINE\SOFTWARE\Lenovo\ShortcutKey\AppLaunch\Ex_97`
   * `HKEY_LOCAL_MACHINE\SOFTWARE\Lenovo\ShortcutKey\AppLaunch\Ex_98`
   * `HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\Teams`
 

[csavalas]:https://github.com/csavalas
[Lenovo Vantage]:https://apps.microsoft.com/detail/9wzdncrfj4mv
[latest release]:https://github.com/OhShoot01/ThinkPad-Hotkey-Fix/releases/
