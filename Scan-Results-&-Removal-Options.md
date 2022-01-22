## Scan Results:
* ### The results of a scan will show lots of information about each comment (which is also stored in the log file):
  * Comment Text (Extremely long comments are truncated after 1500 characters. 'Newlines' are also removed.)
  * Author Name
  * Author's Channel ID
  * The video title (in certain modes)
  * A direct link to the comment

* ### Match Samples List
  * Instead of having to look through every single comment, the program will display a 'sample list' of one comment per matched author
    * Since many scammers just spam the same thing repeatedly, this is a good way to get an idea of the type of comments they're leaving
  * Also shows number of matched comments from the author
  * Duplicate Comments: As a separate sample list, the program will also display commenters who left many nearly identical comments
    * Read more about this feature on the [dedicated page wiki here](https://github.com/ThioJoe/YT-Spammer-Purge/wiki/Duplicate-Comment-Scanning)

## Comment Removal:
* ### Options for Taking Action on Matched Comments:
  * Delete - Exactly what it sounds like
  * Held For Review - Sends the comment to the 'held for review' section in creator studio
  * Report - Report the comment for spam
    * This action is the only action possible if you are scanning someone else's channel

* ### Excluding Commenters From Removal
  * Before removing/reporting the comments, you can choose to exclude all the comments by specific authors, so they will not be removed/reported
    * You tell the program which authors to exclude by using the number next to them in the 'match samples' list
  * You can exclude using either of two following commands when prompted (followed by the authors' numbers from the sample list):
    * `exclude` - Excludes authors by explicitly selecting them
    * `only` - Basically the inverse of exclude. It means you _only_ want to remove/report the specified authors, and exclude the rest
  * Whitelist: When excluding authors, you will also be asked if you want to add them to the whitelist so they won't be flagged in future scans
  * After excluding authors, the log file will be updated:
    * A list of excluded authors will be added at the bottom
    * Excluded authors' comment IDs will be removed from the ID list near the top
      * Note: The comments and other info for these comments will still be in the main list. Just the comment IDs are removed from the list at the top, so they aren't deleted when using the mode that deletes comments using the log file
    