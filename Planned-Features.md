## Currently Planned Features
* v1.6: Search usernames and/or comments based on entire strings, not just individual special characters
* v1.6 or 1.7: Smart Spam Detect: Search usernames and/or comment text for unicode characters used almost exclusively by spammers (such as unicode number characters) - Also allow importing of custom list of characters from a file
* v1.7 or 1.8: Allow use of a config file to more easily run script with repeated settings

## Eventual Planned Features
* Monitoring Mode: Program could be let to continue running and automatically mark matched comments as 'held for review', so they can be restored if incorrectly removed.
* Allow use of command line arguments to be able to run script fully headless

## Whenever I Get Around to It
* "Undo" function - When the program 'deletes' comments, it actually marks them as rejected. If you still have the comment ID, you can actually use the API to mark it as accepted to undo deleting them. Could allow importing a log file from a previous run to undo deleted comments if desired for some reason.
* Graphic User Interface (v2.0)

## Maybe Some Day
* Self-Hosted web version, wouldn't require downloading or setting up your own Google Cloud project
* Auto Full-Scan Mode: Scans entire channel until more than ~100 comments scanned without spammer found, then stops automatically


