## Scanning Mode: Determines _What_ to Scan

<p align="center"><img width="675" alt="Scanning Mode Selection" src="https://i.imgur.com/6QWTP9C.png"></p>

### 1. Specific Videos
   - Input a single video or list of multiple videos (comma separated) to scan
   - Videos must all be from the same channel
   - Accepts input as video link or just the video ID

### 2. Recent Videos For a Channel
   - First asks for a channel to scan. Can be anyone's channel or your own
      - To scan your own channel, you can simply hit Enter (blank entry)
   - Automatically scans a chosen number of most recent videos (up to 500), back to back
       - NOTE: Before scanning huge numbers of videos, be aware of the daily [API quota limit](https://github.com/ThioJoe/YT-Spammer-Purge/wiki/Understanding-YouTube-API-Quota-Limits)

### 3. Recent Comments Across Entire Channel
   - Scans the most recent comment threads across your entire channel (all videos, even stories apparently), but NOT community posts.
   - Casts a wide net, but not great if you want to catch every spammer, because the API returns comment threads based on when the thread was created.
      - Therefore, if a very old top-level comment gets a brand new reply, the reply would probably not get scanned.
   - Requires manual entry of how many comments to scan, because otherwise there is not any real way to tell how long it would take to scan every comment on your channel, if even possible (before using up the daily quota)
   - Only available to be used on your own channel

### 4. Community Posts (Experimental)
   - Experimental because it does not use the YouTube API, but rather a workaround to parse the actual post page
      - Much slower than other modes as a result
   - YouTube's API does not currently allow you to retrieve a list of comments on community posts at all. However, if you have the comment ID for them, you can still delete them, report them, etc.

### 5. Recent Community Posts (Coming Soon, Experimental)