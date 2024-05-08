# Thinkpad Hotkey Fix
### Problem description: [https://www.reddit.com/r/thinkpad/comments/r18cbr/comment/l30weol/](https://www.reddit.com/r/thinkpad/comments/r18cbr/remapping_call_keys_f9_f10_f11/)
### Kudos to [csavalas], who came up with the initial fix! - This is a modified version of his original work.
# 
### Note: This will replace the default actions of the F9 (messages), F10 (answer call) and F11 (hang up call) keys on modern ThinkPads with the following...
#### | F9 - Play/Pause | F10 - Previous song | F11 - Next song |
# 
### Requirements:
* OS: Windows (tested on 10 & 11)
* Have the [Lenovo Vantage] app installed
# 
### Instructions:
* Download the [latest release] and extract the `.zip` file to a folder (NOTE: the folder name should **not** contain spaces.)
* Copy the path of each `ex_9x.vbs` file (*Ctrl + Shift + C* or Right click > Copy as path)
* Open `tp-hotkeys-fix.reg` with notepad.
* Replace the paths for each file accordingly (lines `8`, `15` and `22`). **Do not remove quotation marks from the original file.** You must also replace `\` in the file paths with `\\` | For example: `C:\Users\Oh_Shoot01\hotkeys-fix\ex_98.vbs` would become `C:\\Users\\Oh_Shoot01\\hotkeys-fix\\ex_98.vbs`.
* **If Microsoft Teams is installed on your computer,** delete the last line of code: `[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\Teams]` 
* Save and exit the file.
* Double click the `tp-hotkeys-fix.reg` file.
* Select Yes/OK on any confirmation dialogs that appear.
* Done!

**Extra:** if you wish to hide this folder, you can set it to hidden in its properties menu (select *Apply changes to this folder only* if prompted with a Confirm Attribute Changes dialogue).

### Reference:
* The registry file creates/modifies the following keys:
   * `HKEY_LOCAL_MACHINE\SOFTWARE\Lenovo\ShortcutKey\AppLaunch\Ex_96`
   * `HKEY_LOCAL_MACHINE\SOFTWARE\Lenovo\ShortcutKey\AppLaunch\Ex_97`
   * `HKEY_LOCAL_MACHINE\SOFTWARE\Lenovo\ShortcutKey\AppLaunch\Ex_98`
   * `HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\Teams`
 

[csavalas]:https://github.com/csavalas
[Lenovo Vantage]:https://apps.microsoft.com/detail/9wzdncrfj4mv
[latest release]: 
