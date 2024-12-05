Rom management;

Now that you have your R-Cade system running, lets talk about rom management. Many other systems out there make rom management annoying, requiring you to setup each rom, and each emulator and can be annoying. This doesn’t mean those systems are bad or anything, many are quite good.  But R-Cade takes rom management a step further and makes it far simpler.  All you need do is put the rom in the correct folder for the system it’s for and you’re basically done and usually it just works.  You’ll run into a few cases when this doesn’t work but we’ll get to what you need to do in those cases as some roms don’t run well under the default emulator and require you to change it,  or require a bios to be added.  All of that will be covered in this section.  Also on a side note, if you’ve looked around the menu of rcade already you’ve probably noticed a lack of systems displayed.  Only a very few systems show up in a fresh install. This is normal.  To avoid cluttering the menu with useless options, rcade hides systems you don’t have any roms for by default.  Those menu’s will appear once you’ve added some roms for any systems that are currently not visible.

First, the easiest way to manage your R-Cade roms is via network, although this isn’t the fastest if you had a lot of roms you want to load up. If you have a lot of big roms I suggest copying them to an sd card or usb drive as network file transfers can be slow. So to access your rcade open the network folder for whatever os you’re running.  In windows it’s called network, or my network depending on version. Linux it varies greatly by if you’re using gnome, kde, or other but it’s also usually called network.  Mac you can find it in the finder window, again called network.  In most os’s you can also type \\rcade in a file browser window and it’ll work.  A word of warning, windows usually has network discovery turned off by default.  If this is the case for you, when you go to network in explorer you will see a message bar near the top telling you as much. Click the message bar and windows will offer to turn on sharing/network discovery or mark your current network as private. Marking network as private is the better option for security reasons.  Once you see rcade in network, or see a folder named share, open them.  Once you’re in the share folder you’ll see many folders, the most important two for this guide is bios and roms.

Roms folder; when you open it, you’ll see there’s individual folders for every system that rcade supports.  If you have some roms, just copy them to the right folders. Most of the systems are abbreviated.  N64 for example being Nintendo 64. Add roms to your hearts content. However I’d advise against letting your library grow too large as the current version of rcade is a bit slow at loading huge libraries. We’re always working on improvements so this should change very soon as one of the items being worked on is a much improved library scanner.  Depending on your hardware, I suggest keeping total roms under a couple thousand for best results.  My own personal library is around 200 thousand roms and I can tell you rcade doesn’t play nice on startup yet lol.  But I also discovered having such a massive library on the device makes finding anything you want to play a nightmare anyway.  Best to cherry pick the roms you want and leave out the junk you never play for your own piece of mind as searching so many roms just to find a game to play is annoying. If you need a reference on what file extensions/formats each emulator requires, just look at the text file you find in the folder for that system, file is called ROMS_README.txt.  Once you have some roms in the rom folder, go back to your rcade,  open the menu, and hit reload rom list to rescan your roms. Depending on how many you added, this may take a couple seconds or a couple minutes. Any systems that didn’t show up in menu before will if you’ve added any roms for them as rcade only shows them if you have roms for that system.

Now that you have some roms, lets launch one.  I’ll use n64 as an example but this applies to almost all the emulators. Most roms will play just find right out of the box, but a few you’ll notice very poor performance, or don’t work at all. This isn’t rcades fault, some roms are moody.  The good news is in most cases this is easy to fix.  Most of the time, all you need to do is pick a different emulator.  To do this, highlight the game in question in the menu, and hit the menu button. Select game options, if you don’t see game options you’re in the wrong menu, rcade has two menu’s that can be accessed here.  One using the hamburger button on remote, other using home button.  On most controllers it would be start and select.  If you don’t see game options then leave that menu and try the other button.  Under game options, you’ll see the game emulator option.  By default all roms launch with the default emulator, but you can change this on a per rom basis for those trouble roms that won’t work with the default.  Try a different emulator, in the case of Nintendo 64 you have several to choose from. Just go down the list one at a time till you find one that works best.  In some cases you may also need to enable other options like gate restrictions but try to avoid that if you don’t need it.

Bios folder; If rom still won’t launch, or you have poor performance, then it’s possible it doesn’t like running under the emulated bios. This is often the case with psx games for example. Some games won’t work unless you’re running a real bios. Rcade ships with bios files for some systems, but due to licensing restrictions it can’t include them all so it’s up to you to find them.  To install a bios all you need do is place the files into the root of the bios folder.  In most cases you don’t want them in a subfolder as they won’t be automatically recognized. If you have the correct bios files placed in the bios folder, try launching your game again. If they are the correct files for that system and are in the right place they should be recognized automatically and used instead of the emulated bios. This solves a lot of game compatibility and performance problems, especially with psx games.

Network drive and external storage;  both of these are handled basically the same way with one difference, external drives need to be formatted first, and in the case of a network drive, you need to go to menu, system settings, external device settings, network drive settings. Enter your network drive path, please use ip address in your network path as server name lookups aren’t well supported and may or may not work depending on your environment.  In general, the network path will look something like 192.168.1.10/share/romspath where share is the shared folder on the machine in question, and roms path is the path to the folder you want to store everything in.  Add your username and password if one is required and switch connect network drive to on.  At this point you may want to do a reboot to insure these settings are saved, and to get rcade to attempt to mount folder if it failed to auto mount when you added it. 

Now we need to prepare our external storage if you’re using that instead of a network drive, or you’re using both. Please insert your usb drive, sd card, or bubble gum machine or whatever else you have that can store files into a computer. You may format it in any file system you wish for most part, rcade doesn’t support them all but the list of what it does support is impressive.  For simplicity and speed and wide range of support across devices I suggest exfat.  It’s fast, it’s more reliable than fat32, supports large files and huge drives, and is well supported under rcade.  But you’re welcome to try any system you want.  Worst case is rcade won’t recognize drive and you’ll just need to try a different file system.  Ones I know off hand that work are fat32, exfat, extfs and all it’s incarnations.  Once your drive is formatted, insert it into the rcade device and give it a moment to mount. Rcade may ask you if you want to rescan your roms cause external devices changed. Your answer won’t matter here since there’s nothing on the drive yet. 

Next steps apply to both external and network drives, as from this point forward rcade doesn’t distinguish between the two, treating them both identically. As such I will refer to both as external drives from here on out.

Next we need to prepare our external drive to hold our roms. This step is mostly automatic. I say mostly cause you do need to tell rcade to do it as it won’t modify your drives till you tell it to. Back under external device options, choose prepare external media for rcade.  What this does is creates a copy of the rcades media folder structure onto the drive, and copies important files you may need or want at some point.  This process can take a bit depending on the speed of your external drive so be patient.

Now back to your rcade network share, you will now find inside each rom folder is a folder in parenthesis. Example (usb0).  You may have more than one of these depending on how many external devices you have inserted and prepared properly.  Using n64 as an example again, inside the n64 folder would be a (usb0) folder.  This folder points to the n64 folder on your external drive.  You may use this folder to copy roms directly to your external storage through the network.  Or you can access your external storage directly from your computer by plugging in the drive or accessing the network share you used for the network drive option.  For the most part, you treat this folder exactly as you would internal storage.  Under your emulators menus, you will see these folders as well, named (external0) - usb or something similar. Just pick that to see the list of roms on an external drive.

Scraping rom data and editing menu;  Lets say you added a bunch of roms for Nintendo, or any other system. You open the menu and have this ugly file list with names that can sometimes be cryptic or just plain ugly to look at.  Well this is how you fix that!  Select the rom you want to make look pretty and hit your menu button. Pick edit this items metadata at the bottom of the list. You may edit any of the information you see on this page, or you can scrape it to auto populate these fields.  To scrape, use the scrape button at the bottom. It will run a search on the file name. Depending on the name, this may or many not produce accurate results, or any results at all.  That’s ok, just pick the input button at the bottom of the window and edit the filename. Type in the game name. Sometimes you get more accurate results by omitting details.  Example if it’s tekken 2, try leaving off the 2. Odd as that may sound, sometimes too much information can fail to produce a result, even if the info was right. You’ll see the right option in the list as searching for tekken should list every single version of that game. Select the version from list you think applies to your copy and it’ll pull that data into the metadata window. Click the save button to commit those changes.