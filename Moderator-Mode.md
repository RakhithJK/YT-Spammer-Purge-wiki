## Context Info to Understand
* YouTube accounts that have [moderator permissions](https://support.google.com/youtube/answer/10888907?hl=en) for a particular channel are able to remove ('hide for review') comments on that channel, even via the API
* This program automatically detects when you are scanning content on a channel other than your own
   * It then normally _only_ presents the option to report matched comments
* The program can be overridden with the so-called 'moderator mode', so it will present the option to remove comments (by hiding for review, not permanent removal), even if scanning someone else's channel
   * **Note:** This mode is useless if you do not actually have moderator permissions for the scanned channel. It does not magically allow you to remove comments on a channel for which you don't have necessary permissions; attempting to do so would just cause errors.

## Running the Program With Limited Permissions