## About the Duplicate Scanning Feature
* By default, at the end of Auto-Smart mode and Sensitive-Smart mode, the program will then check for users who left repeated comments
* Comments need not be _exactly_ the same, the program uses an algorithm called _Levenshtein distance_ to detect **similar** comments
* The default settings will flag a user for duplicates if on one video, they make **5 or more** comments that are **>90% similar** to each other

## Customizing Duplicate Settings
### The config file has three settings related to duplicate scanning:
* `duplicate_check_modes` - Allows you to choose which filtering modes will also scan for duplicates
   * You can also disable it completely by entering 'None'
* `levenshtein_distance` - Determines at least how similar two comments must be to be considered a duplicate
   * 1.0 means comments must be 100% the same, 0.5 means 50% similar, etc.
   * If you enter 0.0, it will flag the comments of any user who leaves more comments than the minimum_duplicates setting, regardless of how similar they are
* `minimum_duplicates` - The minimum number of duplicate/similar comments a single user must leave before they are flagged / counted as a match
   * When the threshold is reached, _all_ of the users' comments will be flagged, not just the similar ones


## Where To Find Duplicate Results
* Duplicates are checked separately & after the regular filter mode has run
* The results are displayed at the same time as the rest of the results, but the match samples are separated
* If a commenter was already flagged by the regular filter mode, it wont be also displayed in the duplicate results
   * Therefore the duplicate results show only users who did _not_ match your filter criteria, but are still worth your attention
   * It is a good way to spot spammers who may have gotten around the filter, but also be sure to check for false positives