#### ( Yes, recovering _Deleted_ comments, not just those Held For Review )
***

## How Is This Possible?
* When you 'delete' a comment someone else made on your video, you are not actually deleting it from YouTube's servers
  * You actually are setting the comment's "[moderation status](https://developers.google.com/youtube/v3/docs/comments/setModerationStatus)" to `rejected`
    * Note this is separate from the `heldForReview` status
  * The original commenter will still see the comment on the video, and not know that the comment was deleted (unless they try to view it while logged out)
  * I believe if someone deletes _their own_ comment, it is actually deleted
* If you still have the unique "comment ID" of the comment, then even if you 'deleted' a comment, you can restore it using the API
  * This is done by setting changing the "moderation status" from `rejected` back to `published`
  * Important: You MUST have the original comment ID of the deleted comment to restore it. There is **no way** to look up a list of comments that you deleted from a video
* The log files created by this program does save the IDs of the comments you delete (assuming logging was enabled), therefore allowing you to restore those deleted comments later if you want

### Restoring Comments Using the Program
* In the main menu, you can choose the option to recover deleted comments
* The easiest way to restore comments is by feeding the program the log file that was created after deleting those comments
  * To do so, enter the name of the log file when asked
* You can also manually enter a list of comment IDs to restore if you saved the IDs in some other way, or for some reason the log file isn't working
  * To do so, when the program asks for the name of the log file, just hit Enter without inputting anything
* The program will restore the comments and attempt to check that they were