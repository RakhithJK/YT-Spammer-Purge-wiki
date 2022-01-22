## About the Config File
* Can be used to **pre-set and skip** any prompt or option that the program asks when running
   * Example: You can enter your channel ID in the `your_channel_id` setting, so the app doesn't ask you to confirm your channel every time upon running
* Also contains some settings exclusive to the config file, and cannot be changed in the program itself
* Can be configured to run the program fully autonomously, given all necessary options are set
* Direct Link in Repo: https://github.com/ThioJoe/YT-Spammer-Purge/blob/main/assets/default_config.ini
* If the version at the bottom of this page isn't the latest config version, it probably means I forgot to update this page. Just submit an issue to remind me.

## Multiple Config Files
* You are able to create multiple config files with different sets of favorite settings
* If the program detects multiple config files, it will prompt you which one to use, or none (default settings)
   * The 'main' config is `SpamPurgeConfig.ini`, and additional config files must be named such as `SpamPurgeConfig2.ini`, `SpamPurgeConfig3.ini`
      * The numbers need not be sequential, you can use whatever numbers you want in the file names
* You can create the config file using the "Create config file" option at the main menu, or by just copy and pasting an existing file and renaming it
* You can change the description of a config file shown in the config selection menu by changing the `this_config_description` setting of each file

## List of Config Settings
#### Notes: 
* For complete descriptions and possible values for each, you can look in the [config file itself here](https://github.com/ThioJoe/YT-Spammer-Purge/blob/main/assets/default_config.ini)
* Some config settings are only allowed in certain filtering modes
* Settings marked with a 📝 icon indicates it can only be chosen/set via the config file, and are not prompted for in the program
***

General

* `use_this_config`: Whether to use the config file on launch or not, or ask every time
* `your_channel_id`: Prevents having to confirm logged-in user each run
* 📝`auto_check_update`: Whether to automatically check for updates of program and spam lists upon running
* 📝`release_channel`: Whether to be notified of all new releases (including beta), or only stable releases
* 📝`skip_confirm_video`: Don't ask to confirm the video is correct after entering a video link/ID
* 📝`moderator_mode`: Overrides 'not your channel mode', so those with moderator permissions on a channel have the option to hold comments for review
* 📝`auto_close`: Makes the program close instead of prompt to return to the main menu, after a full scan is complete

Scanning

* `scan_mode`: Sets the scanning mode (_what_ to scan)
* `max_comments`: Maximum number of comments to scan in 
* `video_to_scan`: If chose to scan a video, this sets the video to scan
* `channel_to_scan`: If chose to scan recent videos on a channel, this sets which channel
* `recent_videos_amount`: If chose to scan recent videos, this sets how many (up to 5)

Filtering

* `filter_mode`: Sets the filtering mode (what to scan _for_)
* `filter_subMode`: When searching a comment/username/both, sets whether to search for individual characters, strings, or custom regex
* `channel_ids_to_filter`: In Channel ID Mode - Sets the specific channel IDs / links of users to search for (chan
* `autoASCII_sensitivity`: In ASCII Mode - Sets the sensitivity to use (allow extended ASCII, standard ASCII, or only alphanumeric)
* `characters_to_filter`: (Submode) - Filter for individual characters
* `strings_to_filter`: (Submode) - Filter for words, phrases, sentences, etc
* `regex_to_filter`: (Submode) - Filter using a custom regex expression


Removal

* `skip_deletion`: Sets whether to skip deleting matched comments
* 📝`delete_without_reviewing`: Sets whether to remove comments without 
* `enable_ban`: Sets whether to ban matched users
* `removal_type`: Sets whether to delete, hold for review, or report matched comments
* 📝`check_deletion_success`: Sets whether to check that comments were successfully deleted, to save on time and API quota

Logging
* `enable_logging`: Whether to create log file or not
* 📝`log_path`: Change the path of where the log file is saved
* 📝`log_mode`: Sets the format of the log files, whether Rich Text Format (default) or plaintext
* 📝`json_log`: Whether to additionally also create a json version of the logged match data
* 📝`json_encoding`: Sets the encoding method to be used in the json file
* 📝`json_extra_data`: Whether to add extra information about each comment to the json file
* 📝`json_profile_picture`: Whether to also fetch profile picture thumbnails for matched commenters (while in json logging mode)

Info

* `config_version = 18`: Used to alert user if their config file is out of date