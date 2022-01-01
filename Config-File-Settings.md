## About the Config File
* Can be used to **pre-set and skip** any prompt or option that the program asks when running
   * Example: You can enter your channel ID in the `your_channel_id` setting, so the app doesn't ask you to confirm your channel every time upon running
* Also contains some settings exclusive to the config file, and cannot be changed in the program itself
* Direct Link in Repo: https://github.com/ThioJoe/YT-Spammer-Purge/blob/main/assets/default_config.ini

## List of Config Settings
#### Note: For complete descriptions and possible values for each, you can look in the [config file itself here](https://github.com/ThioJoe/YT-Spammer-Purge/blob/main/assets/default_config.ini)
***

General

* `use_this_config`
* `your_channel_id`
* `enable_logging`
* `log_path`
* `auto_check_update`
* `skip_confirm_video`
* `moderator_mode`

Scanning

* `scan_mode`
* `max_comments`
* `video_to_scan`
* `channel_to_scan`
* `recent_videos_amount`

Filtering

* `filter_mode`
* `filter_subMode`
* `channel_ids_to_filter`
* `autoASCII_sensitivity`
* `characters_to_filter`
* `strings_to_filter`
* `regex_to_filter`


Removal

* `skip_deletion`
* `delete_without_reviewing`
* `enable_ban`
* `removal_type`
* `check_deletion_success`

Info

* `config_version = 12`