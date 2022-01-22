## Filtering Mode: Determines What to Scan _For_

<p align="center"><img width="1000" alt="Filter Mode Selection" src="https://i.imgur.com/OvkA9ve.png"></p>

### 1. Auto-Smart Mode
   - **The Recommended Mode:** Hand crafted filters designed to catch every category of scammer/spammer I become aware of
   - Designed to have an _extremely_ low false positive rate. Any time I come across even a single false positive, I attempt to make adjustments to avoid that condition.
   - Identifies wide range of scammer types, such as WhatsApp scammers and 'sex bot' scammers
   - Detects impersonators
   - Detects scam links (when new scam domains are found being used in spam comments, I add them to a list file on my ['YT-Spam-Domains-List' repository](https://github.com/ThioJoe/YT-Spam-Domains-List), so the app can automatically fetch the latest scam domains)
   - Also uses multi-part scoring algorithm to detect many elusive spammer types that don't have unique characteristics 
### 2. Sensitive-Smart Mode
   - Uses the same checks as Auto-Smart Mode, but certain filtering criteria are more sensitive
   - Good for detecting more elusive spammers, but will probably result in more false positives (anywhere from only a few more, to sometimes WAY more)
### 3. Specific Channel IDs / Links
   - Scan for all comments by a single user, or multiple specific users
   - Takes input as a comma separated list of channel IDs or channel links
### 4. Within Username
   - Specific Special Characters: Emojis, Unicode Symbols, etc
      - Input any number of special characters (no need to be commas separated)
      - Will scan for ANY of the individual characters entered
      - Will ignore basic characters like letters and numbers, even if entered
   - Strings: Words, Sentences, Phrases, etc
      - Input a comma separated list of any number of strings
      - Can be a single word, a sentence which includes spaces, or combination of them
      - Will search for ANY of the items in the list (each item separated by the commas)
   - Custom Regex Pattern
      - Advanced, but extremely powerful
      - Allows you to enter custom regex expressions to search for practically anything you want
      - Read more about regex on [Wikipedia](https://en.wikipedia.org/wiki/Regular_expression)

### 5. Within Comment Text
   - Same three options as #4

### 6. Within Username and Comment Text
   - Same three options as #4

### 7. ASCII Mode (Within Usernames)
   1. Allow Standard + Extended ASCII
   2. Allow Standard ASCII Only
   3. NUKE MODE: Allow ONLY Numbers, Letters, and Spaces