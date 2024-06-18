
SD CARD - SSD - LIGHTROOM AUTO-IMPORT V0.1

Any questions or issues, please email purcellaanthony@gmail.com
---------------------------------------------------------------------------------------------------------------------------------------------------

REQUIRED FOR USE:

	Macbook
	Adobe Lightroom Classic (This only works with Lightroom Classic, not any other versions)
	Shortcuts app (should already be installed as it is a Apple app)
	SD Card/SSD

---------------------------------------------------------------------------------------------------------------------------------------------------

AUTOMATION

	if you are looking to run this as an automation, you will need to download an automation 	
	app, as Mac currently doesn't not support automation natively. 
	I built this using an app called SHORTERY (available on App Store; I believe you need to get the PRO 		
	version which is $10/YEAR)
	I'll go over automation steps later if you are looking to use SHORTERY

---------------------------------------------------------------------------------------------------------------------------------------------------

INSTALLING SHORTCUT

	- Open the shortcut
	- A window will pop up and select "Add Shortcut"
	- To ensure this shortcut works with your device/drives, right click and edit the shortcut
	- *If you don't have scripting enabled, select "Open Preferences", a window on the Advanced tab should come 	   
	up, check "Allow Running Scripts" (it may ask you to locate the Lightroom Classic app)*
	- Once finished with Scripting allow; exit out and right-click the shortcut and click "Edit" and then you should be able to see the  	
	whole AppleScript. You NEED to change a few things for this to work on your computer
		
		- change dcimFolderPath to the folder path of the folder on you SD Card that holds all your photos
		- change sdCardPath to the folder path of your SD card
		- on your hard-drive, add a folder for the imported photos and change the ssdFolderPath to the folder path of the folder you 		
		want to have the photos imported to. I recommend naming it IMPORTED just so it's clear what that folder is intended for. 		
		Nothing will actually be stored here long-term, this is just so there is a folder Lightroom can watch. 
		
		*to find the folder path of a folder, right-click the folder and then hold OPTION, and while holding there will be an option 		
		that says "Copy *folder* as Pathname" Paste that in between the quotes of whichever folder path you are changing in the script
		- then set your fileExtension to what name your file is (ie. ARW, JPEG, RAW, TIFF, PNG, ETC)
		
		Once you change these settings, you should be good to go from here on out! The script itself contains even more info on things 		
		if you want to look into that. Ive also provided a TXT file of the code for backup. When changing the code, you can edit in 		
		the shortcut itself, or you can duplicate that TXT file and then edit in there, then replace that with the code in the shortcut

		if you use different cameras that have different file types, you can always duplicate the shortcut and then just change file 		
		older and file extension to work with whatever types you have without having to change the same shortcut.

---------------------------------------------------------------------------------------------------------------------------------------------------

LIGHTROOM AUTO-IMPORT SETUP

	- Before running the shortcut, have your SSD/hard-drive plugged in and open Lightroom Classic and create your catalog (depending on 	
	your organization of catalogs, you will need to set up the auto-import for every catalog)
	- Go to 'File' -> 'Auto Import' -> 'Auto Import Settings...'
	- First, Choose your 'Watched Folder' (this is the folder on your SSD that you named IMPORTED or whatever you chose to name it)
	- Then, 'Enable Auto Import' up top
	- Then, Choose the designated Move folder (for this, just select your SSD). Name 'Subfolder Name' "AUTO-IMPORTED". This folder will 	
	not be staying here longterm, as the shortcut renames the folder once the photos are imported. This is essentially just moving the 	
	photos from IMPORTED to AUTO-IMPORTED.
	- Then click 'OK'

	Lightroom's Auto-import is now setup, and now you don't need to worry about it until you have a new Catalog.

***********************************IMPORTANT NOTE***************************************

	If you are having an issue where it prompts you to rename the folder before all photos have imported, all photos will not be there.
	This will be because your computer runs a little bit slower and the delay for shortcut to delete the IMPORTED photos will start before
	all the photos are imported. If this is the case, you can go into the code and add a longer delay. Scroll down to where you see 'Eject SD
	Card' and where Lightroom opens for the first time. There is a delay under there. Just change the number to a number that works better for
	your computer

---------------------------------------------------------------------------------------------------------------------------------------------------

YOU ARE NOW ALL SETUP!!!!

	
	The first time you run the shortcut, it will probably ask a couple times for permissions for the shortcut to run. Please accept all 	
	the accessibility windows that come up so you don't get any errors

	Assuming all the folder pathnames are correct you should have no errors. 

	For quick access to the shortcut (if you're not doing automation) you can put right-click the shortcut and add to your Dock. Or with 	
	the shortcut selected, go to 'File' -> 'Export...' and you can save it to your Desktop! You can also rename the shortcut to something 	
	easier to say, and you can ask Siri to run it for you.

	ALWAYS BEFORE RUNNING SHORTCUT, MAKE SURE YOUR SSD IS CONNECTED AND YOUR SD CARD. I would also start it with Lightroom closed so that 	
	way Lightroom doesn't open up the import window but this is not detrimental to the shortcut.  

	Once everything connected, all you need to do is activate the shortcut. And the shortcut will handle everything from there!

	Below, I will include a simple step by step of what exactly the shortcut is doing so you have a better understanding of it, and if you 	
	have any errors you might be able to tell where in the process its wrong and fix (any errors will almost always be if a path for a 	
	folder is incorrect. So make sure to double check all your folder paths are correct.)
	

---------------------------------------------------------------------------------------------------------------------------------------------------

SHORTERY AUTOMATION SETUP

	If you want to automate this process by having the shortcut execute just by plugging in your SD card; below is how to setup SHORTERY 	
	with this shortcut.

	- Download SHORTERY and upgrade to PRO
	- Select 'Add Shortcut Trigger'
	- 'Trigger Type' -> 'Devices'
	- Name whatever you want
	- 'Shortcut' -> Select the name of the shortcut in the list
	- Check 'Enable Trigger'
	- 'Selected Device' -> Select the name of you SD cards (hopefully all you SD cards are name 'Untitled' so you won't need to change 	
	this trigger. You will have trouble with automation if you use different file types/cameras and the SD cards are all named the same. 	
	So, I recommend this really if you just use the same camera with the same file types.
	- 'Event' -> select 'on connect'

	AND THERE YOU GO! Now all you need to do is connect the sd card and SHORTERY will run the shortcut for you. There are probably other 	
	automation apps out there so feel free to see if any other apps work for you! And hopefully one day Mac will support native automation

---------------------------------------------------------------------------------------------------------------------------------------------------

SIMPlE EXPLANATION OF SHORTCUT

	- The shortcut looks into your SD card and looks for the subfolder that you set the dcimFolderPath to
	- it then searches through all the subfolders in that folder, and looks for all the file extensions of the type you set for 		fileExtension
	- It then copies all those files to the folder on your SSD that you set with ssdFolderPath
	- Then it opens Lightroom Classic
	- Lightroom Classic (with the auto-import setup) then imports all the photos and MOVES them to the AUTO-IMPORTED folder
	- it then prompts you to rename the AUTO-IMPORTED folder to whatever you want
	- Then it reminds you to Update the Folder location

AND THATS IT! 
HOPE YOU ENJOY THIS SHORTCUT
