# Filtering Mode: Determines What to Scan _For_

### 1. Auto-Smart Mode
   - **The Recommended Mode:** Hand crafted filters designed to catch every category of scammer/spammer I become aware of
   - Designed to have an _extremely_ low false positive rate. Any time I come across even a single false positive, I attempt to make adjustments to avoid that condition.
   - Identifies wide range of scammer types, such as WhatsApp scammers and 'sex bot' scammers
   - Detects impersonators
   - Detects scam links (when new scam domains are found being used in spam comments, I add them to a list file on my ['YT-Spam-Domains-List' repository](https://github.com/ThioJoe/YT-Spam-Domains-List), so the app can automatically fetch the latest scam domains)
   - Also uses multi-part scoring algorithm to detect many elusive spammer types that don't have unique characteristics 
### 2. Sensitive-Smart Mode
   - Uses same checks as Auto-Smart Mode, but certain filtering criteria are more sensitive
   - Good for detecting more elusive spammers, but will probably result in more false positives (anywhere from only a few more, to sometimes WAY more)
### 3. Specific Channel ID / Link

### 4. Within Username
   - Specific Special Characters: Emojis, Unicode Symbols, etc
   - Strings: Words, Sentences, Phrases, etc
   - Custom Regex Pattern

### 5. Within Comment Text
   - Specific Special Characters: Emojis, Unicode Symbols, etc
   - Strings: Words, Sentences, Phrases, etc
   - Custom Regex Pattern

### 6. Within Username and Comment Text
   - Specific Special Characters: Emojis, Unicode Symbols, etc
   - Strings: Words, Sentences, Phrases, etc
   - Custom Regex Pattern

### 7. ASCII Mode (Within Usernames)
   1. Allow Standard + Extended ASCII
   2. Allow Standard ASCII Only
   3. NUKE MODE: Allow ONLY Numbers, Letters, and Spaces