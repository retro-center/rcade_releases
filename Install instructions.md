WELCOME TO R-CADE!
Here is some community developed documentation to get you started...

The goal here is to get some useful information out there for using R-Cade.

Contributions are welcome, so feel free to issue pull requests for changes and additions!

First off, to all the hackers out there who know what they are doing and want to get started.  The root password by default is retro, you can change it in the gui, ssh is enabled by default,  have fun and goodbye.
As for the rest of us humans who need a little help, lets get started with some install instructions.

Step 1: Download the release for your board.
You need a device capable of running r-cade.  Several are supported, see the releases section for a list of supported devices. Please note, in some cases such as the rock64 board, it’s found in quite a few devices.  So simply because your device isn’t listed doesn’t mean it won’t work, check what board it’s based on and get the closest matching build you can find and see if it works!

Step 2: Burn the release to an SD, eMMC, or USB. 
If you are planning to use eMMC, it may be easier to remove the eMMC module and use a writer to write the image to it.  If you don’t have an eMMC writer, or your module is soldered to the board, or you don’t have one at all (such as a raspberry pi), then follow these instructions to write to an sd card or usb drive exactly as you would the eMMC module. If your device has a soldered in eMMC module, or you lack a writer for it, I’ll walk you through how to install to eMMC later, but be sure to use at least a 16 gig sd card so we have room for a copy of the image.  I suggest using etcher, or Rufus to write the disk as they are faster and easier, but dd works too for those who prefer it.  My instructions will be for etcher. Use what you know and trust. So, attach your eMMC module to the writer board, or insert sd card into a slot / adapter, and plug it into your computer.  Windows, linux, Mac, pencil sharpener it doesn’t matter,  if it has an os etcher probably works on it. Download a copy [it’s full name is balenaEtcher] and install it in your os. Select the image you downloaded, no need to uncompress it first as etcher will handle that for you, select your eMMC module or sd card or usb drive from interface, and hit flash.  Grab coffee, depending on speed of your sd card, reader, usb port and so on this may take a few minutes.  When it’s finished, remove the module/card/drive and insert into your device.  Depending on the device the first boot may take a while as it has some after install setup to do.
NOTE: if you are writing rcade to boot from USB - you *will* also need an operating system either on eMMC or SD that supports USB booting

Step 3: Setup networking.
The next steps require a network connection to your new r-cade installation, and some of the features work best with internet too. If you have an ethernet connection please connect it as it works best and is more reliable than a wifi connection.  Don’t misunderstand, wifi does work, but on some boards and some adapters it can be flakey sometimes.  If you don’t have a cable or prefer wifi, go to network settings in the gui and setup your wifi network.  After setting it up reboot the device. Always reboot from the menu, if you don’t it may fail to save the config changes.  R-Cade will continue retrying to connect to your wifi in the background for a few minutes.  If your device refuses to connect to wifi, as a troublehsooting tip - blank out the password, save it by hitting ok, then enter password again and save again, then reboot again.  Once you successfully get it to connect it’ll usually have no further issues.  In some cases, you may need to go into advanced network settings and add a boot delay to wait for network. 10-20 seconds is usually all that’s needed, and device will wait UP TO the time you set.  If it connects before the full time has passed it won’t keep waiting.

Step 4 (optional): Burn the release to eMMC from the SD card (if you're already running from eMMC, or dont' want to - skip this step)
To install to eMMC module, open your file manager on your computer, find the r-cade device and open the share folder.  Decompress the image you flashed to your sd card and copy it over to the share.  Next connect with any ssh client, most os’s have one built in. The default password is retro.  Type "dd if=imagename of=/dev/mmcblk0" - without the quotes - and replace imagename with the name of the image ending in .img that you copied over. (Note that some boards will use mmcblk1).  This step will take a while as dd is stupidly slow sometimes.  Grab more coffee, pet the cat, feed the dog, or something.  You will know it finished when the prompt returns and it says something about bites written. I suggest typing sync to ensure the write cache is flushed, then unplug your power cable, remove the sd card and plug power back in. Device will go through same setup process as last time. Please repeat step 3 to setup your internet again if you want it.

Congrats on having r-cade fully installed!  In the next chapter we’ll start going over some of the features.

TO BE CONTINUED...
