# developer-setup
Setting up a clean for development environment on you mac laptop or desktop.


## Clean install of macOS
The cleanest way to do this is to create a bootable install drive on an external USB drive to boot from.

### Creating a Boot drive

Step 1. 
Make sure there are no installers already on your device, and you aveh enough room on your computer to download the full installer.
First make sure that you don't already have a macOS installer alread installed on you device. Check in your application folder to make sure that app called "Install macOS [macOS version]". eg. "Install macOS Ventura".

If there is, just drag the icon to the trash, and empty the trash. 

Make sure you have around 16GB spare space on your drive.

Step 2.
Download the full installer.
Open up the terminal application, and run the command
`softwareupdate --list-full-installers`

This should return a list of current installers you can download. Now run the followinf command to install the version of OS you want.
`softwareupdate --fetch-full-installers --full-installer-version [version number goes here]`
eg: `softwareupdate --fetch-full-installers --full-installer-version 13.0`

This will now download a full installer for you selected version. It will take a while, depending on your network speed. 


Step 3.
Connect a USB drive that is at least 16GB in size.

- WARNING
This drive will be erased when you are creating the boot disk, so make sure that is nothing on the drive that you want.

Step 4.
Create the boot drive.

In the terminal run the command.  
`sudo /Applications/Install\ macOS\ [macOS version].app/Contents/Resources/createinstallmedia --volume /Volumes/[USB DRIVE NAME]`

replace `[macOS version]` with the version you are installing, and `[USB DRIVE NAME]` with the name of the drive you making a bootable installer disk 
eg: `sudo /Applications/Install\ macOS\ Ventura.app/Contents/Resources/createinstallmedia --volume /Volumes/untitled`
