🟢 (This page is currently being written, and not finished)
### Important: If you are a large channel dealing with thousands of spam comments, carefully read and understand this page to make your life easier

***

## YouTube API Quotas
* Usage of the YouTube API is not unlimited. For each Google Cloud project you create, there is a default limit of **10,000 "units"/day**.
* The API cost of various actions [can be found here](https://developers.google.com/youtube/v3/determine_quota_cost)
* The "cost" does **not** mean in terms of money, just API usage limits. Using the API is free.

## Effective Quota Usage of This App
* Each comment deleted / reported / hiding costs **1 unit**
* Each comment checked for deletion success costs **1 unit**
   * Note: Checking for comment deletion success can be disabled in the config file. Therefore, if you are handling large amounts of spam, you should probably disable this setting, as it effectively doubles the cost of deleting/hiding each comment.
* Each set of 100 comments fetched costs **1 unit**
* Each set of 5 recent videos _listed_ costs **100 units** (before any comment scanning is even done)

## Calculated Effective Limits of This App (Assuming Default Quota)
* Scan 1,000,000 comments/day
* Delete/Report/Hide 10,000 comments/day
   * If also checking for deletion success: Only 5,000 comments/day
* Fetch list of 500 most recent videos

#### NOTE: The above calculated / estimated limit amounts assuming _nothing_ else is done. For example:
   * If you scan 1,000,000 comments, you would have no remaining quota to actually delete any found comments
   * If you choose to scan your 500 most videos, by the time the program got the list of those videos, you would not have enough quota to even be able to scan the comments