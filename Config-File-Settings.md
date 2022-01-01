## About the Config File
* Can be used to **pre-set and skip** any prompt or option that the program asks when running
   * Example: You can enter your channel ID in the `your_channel_id` setting, so the app doesn't ask you to confirm your channel every time upon running
* Also contains some settings exclusive to the config file, and cannot be changed in the program itself
* Direct Link in Repo: https://github.com/ThioJoe/YT-Spammer-Purge/blob/main/assets/default_config.ini

## List of Config Settings
#### Notes: 
* For complete descriptions and possible values for each, you can look in the [config file itself here](https://github.com/ThioJoe/YT-Spammer-Purge/blob/main/assets/default_config.ini)
* Some config settings are only allowed in certain filtering modes
***

General

* `use_this_config`: Whether to use the config file on launch or not, or ask every time
* `your_channel_id`: Prevents having to confirm logged-in user each run
* `enable_logging`: Whether to create log file or not
* `log_path`: Change the path of where the log file is saved
* `auto_check_update`: Whether to automatically check for updates of program and spam lists upon running
* `skip_confirm_video`: Don't ask to confirm the video is correct after entering a video link/ID
* `moderator_mode`: Overrides 'not your channel mode', so those with moderator permissions on a channel have the option to hold comments for review

Scanning

* `scan_mode`: Sets the scanning mode (_what_ to scan)
* `max_comments`
* `video_to_scan`
* `channel_to_scan`
* `recent_videos_amount`

Filtering

* `filter_mode`: Sets the filtering mode (what to scan _for_)
* `filter_subMode`: When searching a comment/username/both, sets whether to search for individual characters, strings, or custom regex
* `channel_ids_to_filter`: In Chanenl ID Mode - Sets the specific channel IDs / links of users to search for (chan
* `autoASCII_sensitivity`: In ASCII Mode - Sets the sensitivity to use (allow extended ASCII, standard ASCII, or only alphanumeric)
* `characters_to_filter`: (Submode) - Filter for individual characters
* `strings_to_filter`: (Submode) - Filter for words, phrases, sentences, etc
* `regex_to_filter`: (Submode) - Filter using a custom regex expression


Removal

* `skip_deletion`: Sets whether to skip deleting matched comments
* `delete_without_reviewing`: Sets whether to remove comments without 
* `enable_ban`: Sets whether to ban matched users
* `removal_type`: Sets whether to delete, hold for review, or report matched comments
* `check_deletion_success`: Sets whether to check that comments were successfully deleted, to save on time and API quota

Info

* `config_version = 12`: (DO NOT CHANGE) - Used to alert user if their config file is out of date