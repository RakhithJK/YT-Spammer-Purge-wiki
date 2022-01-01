## Scanning Mode: Determines _What_ to Scan

### 1. Specific Video
   - Should be self explanatory
   - Accepts a video link or exact video ID

### 2. Recent Videos For a Channel
   - First asks for a channel to scan. Can be anyone's channel or your own
      - To scan your own channel, you can simply hit Enter (blank entry)
   - Automatically scans up to the 5 most recent videos, back to back
       - The number is 5 because that's the default amount of videos YouTube's API returns without needing to add extra code.
       - It's possible this can be increased later.

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