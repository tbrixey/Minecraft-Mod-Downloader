# Minecraft Mod Updater (Windows 10)

You appear to have stumbled upon my personal minecraft mod updater script. Here is some back story for you! I have a server I run for a group of friends that utilize our own custom set of mods. You can copy this down and change the zip file of mods or do whatever you need to it if you find this useful!

- [FAQ](#FAQ)
- [Instructions](#Instructions)

first some quick faq

### FAQ

1. Why did you not use CurseForge?
   When building a pack for a specific version, (1.16.4) CurseForge can miss some mods due to main Game Version mismatch. For example _Inventory Sorter_.

   > ![](https://i.imgur.com/8Q1Upwz.png)

   This mod works in 1.16.4, but the listed version is 1.15.2. You have to navigate to the Files tab and download 1.16.3 file (beta version, but still)

   > ![](https://i.imgur.com/H9hn7dM.png)

1. Why do this?
   I host the server locally and review/test mods on the server machine. When I want to re-sync all mods I have to inform everyone to 1. delete their mods folder 2. download the new zip file 3. extract it 4. move all new mods to the %appdata% mods folder.
   With this I can inform everyone to download these 2 files somewhere and run `update-mods.bat` whenever I tell them to!

## Instructions

So if you want to set this up for yourself here is what you will do!

1. Download this repo

   > ![](https://i.imgur.com/nNEbUhb.png)

1. Extract the zip you just downloaded

   > ![](https://i.imgur.com/xI3ll9g.png)

1. Next we need to figure out where to host the file that contains a direct download link. Github does that when you tag a release (where mine is hosted). Zippyshare also works well, but only holds files for 30 days and you can't update the file without changing the URL. I'm going to show you how I did it with github because you can update the zip file without altering the download URL.
   3.1. Create a new public github repo.

   > ![](https://i.imgur.com/oAQP5sZ.png)

   3.2. Next click on "tags"

   > ![](https://i.imgur.com/bTXjiZQ.png)

   3.3. Create a new release and fill this form out. The file you upload should **ONLY** contain the `.jar` files (exampled below)

   > ![](https://i.imgur.com/ZDTM6K8.png)

   > ![](https://i.imgur.com/Wmhr5DW.gif)

   3.4.Publish the release. Right click the zip file and "Copy link"

   > ![](https://i.imgur.com/9AaSgai.png)

1. Phew step 4. Back to the directory with the `update-mods.bat`. Right click it and click edit.

> ![](https://i.imgur.com/bA20dKK.png)

1. Change the url in the curl command to the one you copied in step 3.4.

> ![](https://i.imgur.com/RtSkUCT.png)

1. Save it and you are good to go!
