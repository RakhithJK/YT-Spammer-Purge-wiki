### Version Naming Convention ⇨ Release Version = x.y.z
* x = **Major Version**: Major Overhaul / Restructure of Project
* y = **Minor Version**: New Features / Functionality
* z = **Patch Version**: Bug Fixes & Back-End Improvements After Release
* **"-Testing" or "-Beta"** = Pre-Release, Work in Progress
------------------------------------------------------------------------------
## 2.13
	New Features:
		• Multiple Config Files
			• You can now create multiple config files, and select from a list of them when starting the program
			• User can set short description for each config to show in the list
			• Additional configs can be created with the same menu option as when creating the first config
		• Before deleting/reporting, you can now choose to "_only_" process certain authors, and exclude the rest
			
	Other Improvements:
		• Config file updating is now compulsory, with no more need to close program after updating the config file
		• Config backups are now moved to a separate folder in SpamPurge_Resources
		• Now instead of automatically whitelisting excluded authors, it will ask you. With new config option `whitelist_excluded` to avoid the prompt
		• Improved error handling when log file is opened while program tries to write to it. No longer crashes program, but asks user to close it

## 2.12
	Major New Feature: Duplicate & Similar Comment Detection
		• Detect spammers who leave duplicate comments even if they slightly modify every single one of them
		• Uses Levenshtein Distance algorithm for similarity analysis
		• Three New Config Settings:
			• duplicate_check_modes : Enable/Disable duplicate detection on any filter modes
			• levenshtein_distance : Set the similarity threshold for duplicate comment detection
			• minimum_duplicates : Set the how many duplicate/similar comments someone has to leave before they are flagged
			
	Other Big New Features:
		• Now when removing comments using a list/log file, you can choose to only delete some of them, and the program will save your progress, so you can continue where you left off later
			• Ideal for deleting huge lists of comments
			• Automatically saves progress files and allows you to choose them later
		• Now if an error occurs during scanning, such as hitting the quota limit, the program will skip the rest of the scan and create a log file based on the partial scan (no longer forcing you to exit)
		
	Other Improvements:
		• Now when excluding commenters, you can enter ranges of numbers too (such as 'exclude 1, 3-6, 5, 9-10')
		• Whitelist is now re-loaded immediately after excluding authors, so it applies to other scans in same session
		
	Other Changes:
		• Detection of "link spam" (comments where it is nothing but a youtube link) is now disabled by default but can be enabled in the config via new detect_link_spam option

	2.12.0 → 2.12.1:
		• Fixed bug where comments from the channel owner, current user, and whitelist users were not being ignored during duplicate scanning
	2.12.1 → 2.12.2:
		• Fixed UnicodeEncodingError that could occur when creating deletion error log file

## 2.11
	New Features:
		• New Mode: Remove comments using a list / log file. Now if you created a log file but didn't remove the comments, you can later.

	Other Improvements:
		• Now when you exclude an author from removal, their comment IDs will be removed from the list at the top of the log file, making the log file ready to use in the new removal mode
		• Added new 'auto_close' config setting for ending program after finishing scanning
		• Behind the scenes, the script has been split into several files instead of one monolithic file, which should make it easier to maintain
		• Updated filters to improve detection and reduce false positives

## 2.10
	Major New Features:
		• New "return to main menu" ability. Now in most places, instead of hitting Enter to to exit, it will instead return you to the main menu
			• Also at any prompt in the program, you can enter 'x' to return to the main menu
		• Now when updating the config file version, the program will attempt to copy the old settings into the new. It will also create a backup of the old file first.

	Other Improvements:
		• Now when scanning recent videos, finding a live stream, video with zero comments, or comments disabled no longer blocks continuation. It will simply skip that video and notify you.
		• Reworked and consolidated many variables, so the code should be easier to update going forward
	
	2.10.0 → 2.10.1:
		• Fixed community post searching not working
	2.10.1 → 2.10.2:
		• Fix program auto-closing when it's not supposed to (specifically when logging_enabled was not 'Ask' in config)
		• Added new 'auto_close' config setting for ending program after finishing scanning
		• Fixed rare issue where comments with many certain repeating characters would cause extremely slow progress / freezing
		• Updated filters to reduce false positives

## 2.9
	Major New Feature:
		•  You can now scan ANY number of recent videos (up to 500, the maximum YouTube's API will return)
	New Features:
		•  When logging to json file, adds config setting to also fetch additional data about the matched authors, that might be useful for research / AI purposes.
		•  When logging extra json data, has new config setting to download profile picture thumbnails of all matched authors, as well as video uploader


## 2.8
	New Features:
		• Multiple Video Scanning: In the first scanning mode, you can now input an arbitrary list of videos to scan, instead of just a single video
		• Json Logging: New config option to also log results in a json file. Along with another config setting to choose the encoding scheme for the json file
	Other Improvements:
		• Improved error handling, should give better instructions for certain errors
	Patches:
		2.8.0 → 2.8.1:
			• Fixed program checking for spam list updates every run instead of once daily
		2.8.1 → 2.8.2:
			• Fixed bug where program would crash when excluding someone with emojis / unicode in their username
			• Program now better alerts user when comments being disabled is a likely cause for an error

## 2.7
	New Features:
		• PlainText Logging: New config option for plain text logging, instead of rtf
		• Whilelisting: New whitelist file where you can add channel IDs that will be ignored in scans. Users excluded from removal will automatically be added to the whitelist. The file can be found in the SpamPurge_Resources folder.
	Other Changes:
		• The spam_lists folder has been moved into a new folder called SpamPurge_Resources. This resources folder is also where you can find the whitelist file.
	Bug Fixes:
		• Fixed rare problem where lines of text or usernames were missing from the console in the comment outputs or samples
		• Fixed bug that was causing a "note" to be printed for every single comment that was being checked for successful deletion
	Patches:
		2.7.0 → 2.7.1:
			• Fixed crash when logging if no config file exists
		2.7.1 → 2.7.2:
			• Fixed crash when user chooses not to create log file
		2.7.2 → 2.7.3:
			• Added ability for program to retrieve beta releases, and differentiate them when notifying user about update. Also added config file setting to only receive stable channel update notifications
		2.7.3 → 2.7.4:
			• Fixed crash on startup when using old version of config file

## 2.6
	New Features:
		• Support for multiple spam lists that can be updated from online source, so the program can keep up to date with the latest spammers, and not having to update the whole program.
		• See spam that isn't being caught? Learn more about contributing to the spam lists at the dedicated repository! 
	  	  https://github.com/ThioJoe/YT-Spam-Domains-List
	Patches:
		2.6.0 → 2.6.1:
			• Fixed bug where some channel links were incorrectly being accepted as video links
		2.6.1 → 2.6.2:
			• Now in config file, you can set log file output path using both a relative or absolute directory. (Default log directory is now 'logs')
			• Fixed bug where usernames were not being scanned properly, missing many spam comments

---------------------------------------------------------------------------------------------	
## 2.5

	New Features:
		• Ability to automatically download latest exe file version
	Other Improvements:
		• New spam domain list detection ability, using crowd sourced list of domains used in scam comments (see here:
		• Spam Domain List auto updates itself
		• Improved channel/video link validation
	Patches:
		2.5.0 → 2.5.1:
			• Fixed crash on startup from spam list updating
		2.5.1 → 2.5.2:
			• New config setting allowing you to disable checking for comment deletion success, to save on time and API quota when deleting large amounts of spam.
		2.5.2 → 2.5.3:
			• Fixed crash when "auto_check_update = False" in config file
		2.5.3 → 2.5.4:
			• Revamped method of auto-updating spam lists
			• Added checking for spam list updates when user manually selects 'check for updates'
		2.5.4 → 2.5.5:
			• Added progress percentage when scanning videos, by fetching the total number of comments on videos being scanned

---------------------------------------------------------------------------------------------	
## 2.4

	Major New Features
		• *Experimental*: Community Post scanning and filtering! (Very epic) 👏
	Other Fixes and Changes
		• Filter updates to catch more scammers
	Patches 
		• 2.4.0 → 2.4.1: Can now input community post links, not just exact post IDs
		• 2.4.1 → 2.4.2: No longer ask for max comments when scanning community post (but allow config setting). Also Fixed version number.

---------------------------------------------------------------------------------------------	
## 2.3

	New Features
		• Add config setting for custom log file path
	Bug Fixes
		• Critical: Fix incorrect config file being packaged with 2.2.6 release, causing errors
		• Fixed program displaying warning about config being out of date, when there is no config file at all
	
---------------------------------------------------------------------------------------------	
## 2.2

	Major New Features
		• New 'Recent Videos' scanning mode: Scan up to the 5 most recent videos on a channel back to back!
	Other New Features
		• Program will now notify you when your config file is not the latest version and may cause errors
	Patches
		2.2.0 → 2.2.1
			• Fix issue where creating config file could cause crash on some computers with different languages
		2.2.1 → 2.2.2
			• Fixed recovery mode not working
			• Fixed crash when searching special characters via GUI in Windows
			• Fixed crash when printing to log file in AutoASCII Mode 
		2.2.2 → 2.2.3
			• Fixed bug where program would ask you to enter channel link, even if set to 'Mine' in config file
			• Updated exception message to explain error when scanning a live stream
			• Patch:  2.2.3 → 2.2.4
			• Improved false positive matching of channel usernames. Original behavior moved to sensitive mode
		2.2.4 → 2.2.5
			• Added error message when API quota is exceeded, instead of just crashing
			• Also should prevent crashing in some other previously uncaught errors
	
---------------------------------------------------------------------------------------------	
## 2.1

	New Features
		• New 'moderator mode' option in config: Overrides the 'not your channel' mode, and allows those with moderator permissions to use Auto modes to hold spam comments for review on that channel
		• New option to easily choose most recent video when asked to enter video ID to scan
	
---------------------------------------------------------------------------------------------	
## 2.0.0-Beta

	Major New Features:
		• Ability to create config file and run program completely autonomously, including deletion of comments for certain modes
			• Program gives option to create default config file automatically, user can change as many or few settings as they wish
		• Now able to scan both comment text and usernames simultaneously using any of the filtering sub-modes
		• New 'Recovery Mode' option to re-instate previously deleted comments. Requires the log file from when they were deleted, or at least the list of comment IDs.
		• Now able to choose removal type, either 'Hold For Review', 'Delete', or even just report comments for spam. Anyone can now report spam comments on other peoples' channels (using auto smart mode only)
		• Added "match samples" at end of printing comments list to easily spot false positives. Sample prints only 1 comment per author found, each in one line. In log file, also prints each author's channel ID
		• Ability to exclude selected users before deletion or reporting
		
	Other New Features
		• Program now auto checks for updates (can be disabled in config), and also has manual update checking
	
	
	Other Improvements
		• Auto Smart Mode Improvements:
			• Now searches both comment text and author usernames
			• Adds logic to avoid false-positives from users mentioning spammers when replying to them
			• Now even smarter with additional detection methods
		• Program now completely ignores the current user's own comments
		• MUCH faster displaying results and writing them to log file (bottleneck is now mostly the YouTube API)
		• Program will automatically create an error log file if a deletion fails
	
	Bug Fixes:
		• MacOS Only: The GUI component (searching individual special characters) should work now, but requires manually installing the latest python version.
	
	Beta Update: Beta2 → Beta3
		• New "Sensitive Smart" Mode: Runs mostly the same tests as Auto Smart Mode, but with a much lower threshold to identify a spam comment. Catches more spammers at the cost of more false positives.
		• Improvements to Auto Smart mode, now catches additional types of spammers
	
	Beta Update:  Beta1 → Beta2
		• MASSIVE Upgrades to Auto-Smart Mode: Now also detects sex spam bots with very high accuracy
			• Huge amount of filtering logic added to find the large variety of these types of bots
		• Auto-Smart mode can now detect bots with look-alike usernames
		• Sample list now shows number of comments by each author
		• Better detection of potential false positives from replies
		• Filter now ignores uploader's comments regardless of who is scanning
		• Bug Fix: Fixed program not closing when it's supposed to after checking for updates
		• Bug Fix: Fixed incorrect removal of certain characters from scanning strings
	
---------------------------------------------------------------------------------------------		
## 1.6

	Major New Features:  
		• 5 New Scanning Modes
			• Scan usernames for string or list of strings
			• Scan usernames with any custom regex expression
			• Scan comment text for string or list of strings
			• Scan comment text with any custom regex expression
			• Auto Smart-Mode: Automatically scan usernames for pre-made set of special characters almost exclusively used by scammers

---------------------------------------------------------------------------------------------	
## 1.5

	Major New Feature:
		• Colors
		• Multiple new search modes:
			• Scan usernames or comments text for individual characters
			• Auto-search usernames for non-ascii characters. Three levels of filtering sensitivity:
			1. Allow Standard + Extended ASCII 
			2. Allow Standard ASCII Only
			3. NUKE Mode (┘°□°)┘≈ ┴──┴ 	• Allow only letters, numbers, and spaces
		
	Fixes & Improvements:
		• Now shows progress in terms of numbers when deleting comments and checking after deletion
		• Improved video ID URL checking with regex
		• Improved error handling, such as when token does not match client secret
		• New format/layout when printing comments to console and log file to make it easier to read

	Patch Version:  1.5.0 → 1.5.1
		• Fixed critical new bug in 1.5.0 that displayed wrong comments when printing/logging results
		• Changed "spammers" to say 'matched' in some places to more accurately reflect results meaning
		• Fixed angry throwing emoji to be command prompt display-able (code page 437 character set)
		• Added dividers in log and when printing comments for easier reading text content
		• Added author channel ID to print/log results to more easily make list of spammer IDs

	Other Patches:  
		• 1.5.1 → 1.5.2
			• Added colors
		• 1.5.2 → 1.5.3
			• Fix console clearing command on non-Windows machines

 
---------------------------------------------------------------------------------------------	
## 1.4

	New Features:
		• Scan for multiple spammers simultaneously by pasting in a comma separated list of channel IDs or links
		• Option to ban the spammers when deleting their comments, and log choice to file

	Fixes & Improvements:
		• Better handling in certain cases of expired credentials
		• Compiled pyinstaller bootloader myself 	• no more stupid false positives on VirusTotal 🥳
		• New main() function to run primary code
		• Bug fix for deleted / non-existent channels whose comments remain on video
		• If user doesn't want to continue as logged-in user, automatically prompts new login
	
	Patch Versions:
		• 1.4.0 → 1.4.1
		 	• Improved error handling to more easily identify bugs. Addressed issue if token.pickle for wrong user is used.

---------------------------------------------------------------------------------------------	
## 1.3

	New Features:
			• Now also supports just pasting a channel link or video link, instead of only Video ID or Channel ID	
			• Now automatically fetches current user's channel ID so it doesn't need to be entered

	Fixes & Improvements:
			• Remove many unnecessary packages from requirements.txt
			• Added shebang line for easy execution in linux
			• If trying to scan someone else's video, warns can only delete comments on your own videos
	Patch Versions:
			• 1.3.2 → 1.3.3
			 	• Fixed bug that caused crash when logging certain complex characters to log file (such as unicode or Japanese characters)
			• 1.3.1 → 1.3.2
			 	• Fix closing too fast if user doesn't confirm logged-in account
	
	
---------------------------------------------------------------------------------------------	
## 1.2

	New Features:
        	• Now also allows logging spam comments to text file
		
	Fixes & Improvements:
			• Fixed Oauth2 credential refreshing, no longer requires re-authorizing every hour
			• On invalid inputs, now allows re-try instead of exiting whole program
			• Now displays exact up-to-date stat counts instead of every 100 comments
			• Improved efficiency of printing comments when in single-video mode
			• Better error handling for certain errors
			• Removed unused fields in API requests
		
		
---------------------------------------------------------------------------------------------		
## 1.1

	Fixes & Improvements:
			• Fixed major bug preventing ability to delete comments
			• Better use of API to bulk delete comments instead of individually, to greatly improve quota usage
	
	New Features:
			• Now scans top level comments, not just replies
			• Now attempts to automatically check if comments were successfully deleted
			• On invalid inputs, now allows re-try instead of exiting whole program
			• Now also allows logging spam comments to text file		
		
		
---------------------------------------------------------------------------------------------			
## 1.0.2:

		• Fixed major bug where program would fail if more than 50 spam comments were found
		• Added file version and info to startup messaging		