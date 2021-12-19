To run the script on a Mac, you'll have to download and install Python (the programming language the app was made with).

1. Go to `https://www.python.org/downloads/` and download whatever the latest version is

![Python Download Page](https://i.imgur.com/8BDvUhZ.png)


2. Run the installation `.pkg` file from the downloads folder (or wherever you put it)

![Python Package File](https://i.imgur.com/jT2dXqH.png)


3. When running the installer, you can just continue through keeping all the default options.

![Python Installer](https://i.imgur.com/FNB2jtn.png)


4. Go to the latest on the [Release Page](https://github.com/ThioJoe/YouTube-Spammer-Purge/releases) and download the "Source Code (Zip)" folder. Extract it if necessary.

5. You'll want to enable a MacOS feature to let you open the Terminal through the right-click menu. To enable this feature, you can follow the instructions in this article: [https://www.maketecheasier.com/launch-terminal-current-folder-mac/](https://www.maketecheasier.com/launch-terminal-current-folder-mac/)

5. Within the downloads folder (or wherever), "Right Click" (Control + Click) on the folder with the files in it. Go down to Services > Click "New Terminal at Folder". 
	* Now the terminal should open and show the downloaded folder as being active.

![Opening terminal to folder](https://i.imgur.com/uCml3Ej.png)

6. Now we need to install the necessary modules to run the Python program. Run `pip3 install -r requirements.txt`
	* If it doesn't spit out a whole bunch of errors messages, it should be good

10. Now you can run the program by running: `python3 YouTubeSpammerPurge.py`
	* You can rename the `.py` script file to something more shorter if you want
	* Whenever you want to run it again, open the terminal to that folder the same way by Right Clicking > Services > New Terminal at Folder

11. Remember, you will need to get an API key in the form of a `client_secrets.json` file for the program to work. 
	* Instructions can be found on the [main project page here](https://github.com/ThioJoe/YouTube-Spammer-Purge#instructions---obtaining-youtube-api-key)
	* Or watch the [video tutorial here](https://www.youtube.com/watch?v=-vOakOgYLUI&t=693s) (go to 11:33)

