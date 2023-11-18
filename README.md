# Genshin Notes

## Table of Contents
- [What is this?](#fix-for-blurrinessresolution-in-game)
- [Fix for "blurriness"/resolution in game](#fix-for-blurrinessresolution-in-game)
- [Backup/transfer game data / reinstall game without redownloading](#backuptransfer-genshin-game-data--reinstall-genshin-without-redownloading)

## What is this?
I made this repository to keep info/solution related to [this reddit thread](https://www.reddit.com/r/PocoPhones/comments/16qco4n/poco_f5_genshin_resolution_problem/). Made the name genshin-notes since it might contain information that is useful for other things that is not directly related to it.

### The problem
I encountered problem described in this reddit thread: [POCO F5 Genshin resolution problem](https://www.reddit.com/r/PocoPhones/comments/16qco4n/poco_f5_genshin_resolution_problem/). After some testing, I believe spoofing your device to a different model can fix it. I use the word "believe", because when I compare the screenshots before and after the fix, it looks same. However, the screenshot after the fix definitely looks poor compared to what I actually see in-game. I have compared the game's graphics (after fix) to iPad 8 and OnePlus 7 Pro, it looks comparable. Just a bit uncertainty if I actually had the problem (before the fix). I don't feel like rebooting and reinstalling the game to do the comparsion again :')

# Fix for "blurriness"/resolution in game
Requirements:
- Must have LSPosed/Xposed

Steps:
- Install [this apk](https://github.com/redzuone/Game-Unlocker/blob/a1bc78d66aa4145d8d500e0f560e502df1b2bf94/app/build/outputs/apk/debug/app-debug.apk)
- Open LSPosed, activate the module, Genshin should be selected automatically
- Restart phone
- Clear app data or reinstall game. If you don't want to redownload the game (about 20 GB), see below to see instructions on keeping the game data
- Done. Hopefully it works for you!

# Backup/transfer Genshin game data / reinstall Genshin without redownloading
This operation require you to access Android/data folder. The goal here is to make sure Android/data/com.miHoYo.GenshinImpact/files/ doesn't get deleted when you uninstall/clear the game, and copy it to the game's folder after it is installed/cleared.
The steps you need to take might be different than mine. Newer Android version and some manufacturer might mess with your access to the folder.
Here are the steps I took:
1. Use a file explorer with root access. I use MiXplorer. Navigate to /root/sdcard/Android/data/
2. Rename the folder "com.miHoYo.GenshinImpact" into something else. I added a letter: `com.miHoYo.GenshinImpactO`
3. Uninstall or clear game data
4. Open the game, login, let it download a bit
5. Exit the game
6. Copy the folder `files` from the folder you previously renamed (in this case, `com.miHoYo.GenshinImpactO`), to Android/data/com.miHoYo.GenshinImpact/
7. Merge and overwrite when asked
8. Open game. Congrats! Hopefully you saved some time :>
