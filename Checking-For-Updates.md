### Automatic Update Checking
* Upon running, the program will automatically check for program and spam list updates, and will notify you (in the Scanning Mode Menu / Main Menu) if there is a new version
* Automatic update checking can be disabled via the config file setting: `auto_check_update`
* You can also manually check for updates (such as when automatic checking is disabled) by selecting that option in the Main Menu

### Automatic Update Downloading
* You can have the program download the latest .exe version for you
* This option will be presented after you use the 'Check For Updates' option in the Main Menu
   * The program will also verify the downloaded file's hash to verify it was downloaded correctly

### Spam List Updating
* The program also uses crowd-sourced spam lists in addition to the built in filters
  * You can see the GitHub page for these lists here: https://github.com/ThioJoe/YT-Spam-Lists
* The program will automatically fetch any new spam lists if yours is out of date. It is set to only check once a day, to limit API queries

### Config File Updating
* The program will automatically detect if your config file is not the latest version, and will automatically upgrade yours for you
* It should copy all your previous settings to the new config, but just in case, it will also store a backup of your old config in the  `SpamPurge_Resources/User_Config_Backups` folder