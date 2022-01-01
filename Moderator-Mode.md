## Info to Understand First
* YouTube accounts that have [moderator permissions](https://support.google.com/youtube/answer/10888907?hl=en) for a particular channel are able to remove ('hide for review') comments on that channel, even via the API
* This program automatically detects when you are scanning content on a channel other than your own
   * It then normally _only_ presents the option to report matched comments
* The program can be overridden with the so-called 'moderator mode', so it will present the option to remove comments (by hiding for review, not permanent removal), even if scanning someone else's channel
   * **Note:** This mode is useless if you do not actually have moderator permissions for the scanned channel. It does not magically allow you to remove comments on a channel for which you don't have necessary permissions; attempting to do so would just cause errors.

## Running the Program With Limited Account Permissions
* Many creators may not wish to grant the program such high level permissions normally required to run the program
* Instead, you could create a brand new empty 'dummy' Google/YouTube account, grant _that_ account moderator permissions on your main channel, then just log into the program using that 'dummy account'.
   *Then enable 'moderator mode' in the config settings to you will have the option to hide matched spam comments for review

## Limitations of 'Moderator Mode'
* You won't be able to _ban_ users while removing their comments, as you will not have the permissions
   * You could still go into the 'held for review' section of YouTube Studio, find the spammers, and ban them through there
* I have currently made it so even if Moderator Mode is enabled, you can only remove comments on someone elses channel when using 'Auto-Smart' and 'Sensitive-Smart' filter modes
   * This is because of the potential for abuse (or accidental misuse) of the other filtering modes (such as 'nuke mode') even by those trusted with moderator permissions
   * If you are looking to use 'moderator mode' on _your own channel_ and would like to use other scanning modes, you can contact me for help