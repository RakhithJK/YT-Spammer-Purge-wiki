### ⚠️Important⚠️:  If you're a larger channel dealing with thousands of spam comments, to make your life easier, read and understand this page!

***

## Basic Info: YouTube API Quotas
* Usage of the YouTube API is not unlimited. For each Google Cloud project you create, there is a default limit of **10,000 "units"/day**.
* The API cost of various actions [can be found here](https://developers.google.com/youtube/v3/determine_quota_cost)
* The "cost" does **not** mean in terms of money, just API usage limits. Using the API is free.
* The daily quota resets at Midnight in Pacific Time

## This App's Quota Usage (Average)
* Each comment deleted / reported / hiding costs **1 unit**
* Each comment checked for deletion success costs **1 unit**
   * Note: Checking for comment deletion success can be disabled in the config file. Therefore, if you are handling large amounts of spam, you should probably disable this setting, as it effectively doubles the cost of deleting/hiding each comment.
* Each set of 100 comments fetched costs **1 unit**
* Each set of 5 recent videos _listed_ costs **100 units** (before any comment scanning is even done)

## This App's Calculated Daily Limits (Assuming Default Quota)
* Scan 1,000,000 comments
* Delete/Report/Hide 10,000 comments
   * If also checking for deletion success: Only 5,000 comments
* Fetch list of 500 most recent videos

#### NOTE: The above calculated / estimated limit amounts assuming _nothing_ else is done. 
   * _For Example:_
      * If you scan 1,000,000 comments, you would have no remaining quota to actually delete any found comments
      * If you choose to scan your 500 most videos, by the time the program got the list of those videos, you would not have enough quota to even be able to scan the comments

***

## Requesting An API Quota Increase
   * There is actually a process by which you can request an increase to your project's API quota
   * However, the [request form](https://support.google.com/youtube/contact/yt_api_form) is very elaborate, and I'm not sure they would grant an increase  for most people
      * However, if you are a large channel, I imagine you could work with a partner manager to help you through the process or help you get approved for example

## Quota Limit Work-Around: Multiple Google Cloud Projects
   * The quota limit of 10,000 is for each project you create (which is what you did when you followed the "obtaining an API key" tutorial)
   * You could theoretically create multiple projects in the Google Cloud console (following the same procedure), where each would generate it's own `client_secrets.json` file
      * You can think of the `client_secrets.json` file as the API key
   * Meaning if you run out of quota for one project / api key, you could swap out the `client_secrets.json` file with that of a different project
      * What you'd probably do is rename each one to something like `client_secrets1.json` or `client_secrets2.json`, then whichever one you want to use at the time, rename it to `client_secrets.json`

