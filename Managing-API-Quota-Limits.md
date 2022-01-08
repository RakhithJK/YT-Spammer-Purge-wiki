🟢 (This page is currently being written, and not finished)

## YouTube API Quotas
* Usage of the YouTube API is not unlimited. For each Google Cloud project you create, there is a default limit of **10,000 "units"/day**.
* The API cost of various actions [can be found here](https://developers.google.com/youtube/v3/determine_quota_cost)
* The "cost" does **not** mean in terms of money, just API usage limits. Using the API is free.

### Important: If you are a large channel dealing with thousands of spam comments, carefully read and understand this page to make your life easier

## Effective Quota Usage of This App
* Each comment deleted / reported / hiding costs **1 unit**
* Each comment checked for deletion success costs **1 unit**
   * Note: Checking for comment deletion success can be disabled in the config file. Therefore, if you are handling large amounts of spam, you should probably disable this setting, as it effectively doubles the cost of deleting/hiding each comment.
* Each set of 100 comments fetched costs **1 unit**
* Each set of 5 recent videos _listed_ costs **100 units** (before any comment scanning is even done)

