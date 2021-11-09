# Linux Installation Instructions

1. Download the source code `tar.gz` from the latest release 

2. Extract it into a folder somewhere somewhere

3. Right Click inside the folder > Open in Terminal

4. Check python version. Run: 
 	* `python3 --version`
	* Anything Python 3.x should run - Ideally 3.9.x but 3.8.x seems to work too

5. Check if pip installed - Run: 
	* `pip` or `pip3`
	* If not installed run: `sudo apt install python3-pip`

6.  Install dependencies. Run:  
	* `pip3 install -r requirements.txt`

7. Run the script: 
	* `python3 YouTubeSpammerPurge.py` (possibly case sensitive, you can just rename it)

8. Remember: To use it, you need an API key in the form of a `client_secrets.json` file
	* See instructions in [the ReadMe](https://github.com/ThioJoe/YouTube-Spammer-Purge#instructions---obtaining-youtube-api-key)
