## Scan Results Logging
* After a scan, you have the option to generate a log file with all the results, which is **HIGHLY** recommended
* Log files can be used by other features such as comment recovery and log-based comment removal
* You can also create JSON formatted log files, which may make it easier for analyzing data from the results

## Info Stored in Log Files
* The filtering mode used
* The number of matched comments
* A list of the comment IDs of all matched comments
* The match-samples list, showing one comment from each author
* The list of duplicate commenters
* Whether you chose to ban the commenters
* What action you took on the commenters (removed, held for review, reported, etc)
* A list of every matched comment, each with:
  * Author Name
  * Author's Channel ID
  * Comment Text
  * The video title (in certain modes)
  * A direct link to the comment

## Logging Related Config Settings
* `enabled_logging` - Whether to enable/disable logging without asking
* `log_path` - The folder into which log files will be placed
* `log_mode` - Whether to create log files in Rich Text Format (default) or Plaintext

## JSON Logging Settings
* In the config file you can also find several JSON logging options in addition to the normal logging:
* `json_log` - Whether to also create a JSON based log file with the same info as a standard log file
* `json_extra_data` - Whether to collect additional data for the JSON log file, such as Video Uploader's Name, and Video Title (regardless of scanning mode)
* `json_profile_picture` - The program can also fetch the profile pictures of each commenter and the video uploader, which may be useful for training AI to spot certain types of spammers, such as impersonators
* `json_encoding` - At the moment I don't think this actually does anything, so it will likely be removed if I remember to
