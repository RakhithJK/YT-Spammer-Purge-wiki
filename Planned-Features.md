## Currently Planned Features
* v1.7 or 1.8: Allow importing of custom list of characters or strings from a file
* v1.7 or 1.8: Allow use of a config file to more easily run script with repeated settings

## Eventual Planned Features
* Monitoring Mode: Program could be let to continue running and automatically mark matched comments as 'held for review', so they can be restored if incorrectly removed.
* Allow use of command line arguments to be able to run script fully headless

## Whenever I Get Around to It
* "Undo" function - When the program 'deletes' comments, it actually marks them as rejected. If you still have the comment ID, you can actually use the API to mark it as accepted to undo deleting them. Could allow importing a log file from a previous run to undo deleted comments if desired for some reason.


## Maybe Some Day
* Graphic User Interface (v2.0)
* Self-Hosted web version, wouldn't require downloading or setting up your own Google Cloud project
* Auto Full-Scan Mode: Scans entire channel until more than ~100 comments scanned without spammer found, then stops automatically


