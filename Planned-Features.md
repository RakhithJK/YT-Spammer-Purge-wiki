## Currently Planned Features
* Add 'only' option, like an opposite of 'exclude' - Only delete certain users from sample
* Ability to delete comments using a list of comment IDs, such as from a log file
   - For large amounts of comments that require multiple sessions (because of API quota), it could keep track of which were deleted and which still need to be deleted

## Relatively Soon™
* Option to search also obfuscated versions of entered strings
* An option to delete comments using just a list of comment IDs - Could be useful if too many comments are found for your quota limit, and the job needs to be continued where it left off
* Break the script up into multiple files, as it is becoming absolutely enormous
* Add scan recent community posts

## Whenever I Get Around to It
* Monitoring Mode: Program could be let to continue running and automatically mark matched comments as 'held for review', so they can be restored if incorrectly removed.
* Channel 'Mega-Scan' - Automated process to scan all comments on every single video on a channel.
   * Could theoretically pre-calculate the total number of comments needed to be scanned, and determine how many could be done in one go
   * Would need to implement a way to continue where left off, allowing user to either switch to a different google cloud project, or wait until the next day's quota reset

## Maybe Some Day
* Self-Hosted web version, wouldn't require downloading or setting up your own Google Cloud project

## Not likely
* Graphic User Interface


