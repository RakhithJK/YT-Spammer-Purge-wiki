## Confirmed for Next Release 2.0 (And already available in .py script version)
* Allow importing of custom list of characters or strings from a file
* Allow use of a config file to more easily run script with repeated settings
* Allow running program with no user interaction via config file
* "Undo" / Recovery function - When the program 'deletes' comments, it actually marks them as rejected. If you still have the comment ID, you can actually use the API to mark it as accepted to undo deleting them. Allow importing a log file from a previous run to undo deleted comments if desired for some reason.
* Auto check for updates and notify if new version available

## Currently Planned Features
* Report-Only Mode (If Possible): Makes the program useful even to viewers, and would allow scanning their favorite creators videos/channels and reporting spammers.

## Eventual Planned Features
* Monitoring Mode: Program could be let to continue running and automatically mark matched comments as 'held for review', so they can be restored if incorrectly removed.
* Command line arguments

## Whenever I Get Around to It


## Maybe Some Day
* Graphic User Interface (v2.0)
* Self-Hosted web version, wouldn't require downloading or setting up your own Google Cloud project
* Auto Full-Scan Mode: Scans entire channel until more than ~100 comments scanned without spammer found, then stops automatically


