To run the script on a Mac, you can install Apple's "Command Line Tools" which includes Python 3, which runs the program.

1. Search for and open the 'Terminal' app. Don't worry, it's not as scary as it looks.

2. Type in `python3` and hit Enter. It should prompt you to install the command line tools, so click 'Install'.

3. Wait for it to download. It might say it will take ages but it won't. My Wi-Fi was being very slow and it took about 15 minutes. Afterwards, you can close the terminal for now.

4. Go to the latest on the [Release Page](https://github.com/ThioJoe/YouTube-Spammer-Purge/releases) and download the "Source Code (Zip)" folder. Extract it if necessary.

5. Within the downloads folder (or wherever), "Right Click" (Control + Click) on the folder with the files in it. Go down to Services > Click "New Terminal at Folder". 
	* Now the terminal should open and show the downloaded folder as being active.

6. Now we need to install the necessary modules to run the Python program. Run `pip3 install -r requirements.txt`

7. You might see a whole bunch of error messages come up. Near the bottom it might say something like:
 	*  `ImportError: cannot import name 'PackageFinder' from 'pip._internal.index' `
	* If this happens don't worry, continue to step 8

8. Next we can make sure the command line tools are up to date (even though they just downloaded, they might not be). 
	* Run: `softwareupdate --list`
	* Look if you see something like: `* Label: Command Line Tools for Xcode-13.0`
	* If so, run: `softwareupdate -i "Command Line Tools for Xcode-13.0"` (or whatever it says for you as the command line tools label)
	* It should download and install, then say Done. It might take several minutes.

9. Try running the command again: `pip3 install -r requirements.txt`
	* If it doesn't spit out a whole bunch of errors messages, it should be good

10. Now you can run the program by running: `python3 YouTubeSpammerPurge.py`
	* You can rename it to something more convenient if you want
	* Whenever you want to run it again, open the terminal to that folder the same way by Right Clicking > Services > New Terminal at Folder

11. Remember, you will need to get an API key in the form of a `client_secrets.json` file for the program to work. 
	* Instructions can be found on the [main project page here](https://github.com/ThioJoe/YouTube-Spammer-Purge#instructions---obtaining-youtube-api-key)
	* Or watch the [video tutorial here](https://www.youtube.com/watch?v=-vOakOgYLUI&t=693s) (go to 11:33)

