# Automatic Installation
- (Supports Ubuntu/Debian-based, Arch/Arch-based, and RPM-based Distributions)
1. Download [install.sh](https://raw.githubusercontent.com/ThioJoe/YT-Spammer-Purge/main/install.sh)
	* This script will install dependencies, and a copy of [YT-Spammer-Purge](https://github.com/ThioJoe/YouTube-Spammer-Purge/).
	* Run: `curl https://raw.githubusercontent.com/ThioJoe/YT-Spammer-Purge/main/install.sh -o install.sh`
2. Make the bash script executable. Run:
	* `chmod +x install.sh`
3. Finally, execute the script. Run:
	* `./install.sh`
# Manual Installation
1. Download the source code `tar.gz` from the latest release 

2. Extract it into a folder somewhere somewhere

3. Right Click inside the folder > Open in Terminal

4. Check python version. Run: 
 	* `python3 --version`
	* Anything Python 3.x should run - Ideally 3.9.x but 3.8.x seems to work too

5. Check if pip installed - Run: 
	* `pip` or `pip3`
	* If not installed run: `sudo apt install python3-pip`(This is for Ubuntu/Debian-based distributions. For other distributions, try the automatic installation or use the distribution's own package manger.)

6.  Install dependencies. Run:  
	* `pip3 install -r requirements.txt`
7. Install the tkinter library. Run:
	* `sudo apt-get install python3-tk`
# Running The YouTube Spammer Purge application
1. Run the script: 
	* `python3 YTSpammerPurge.py` (usually case sensitive, you can just rename it)

2. Remember: To use it, you need an API key in the form of a `client_secrets.json` file
	* See instructions in [the Wiki here](https://github.com/ThioJoe/YT-Spammer-Purge/wiki/Instructions:-Obtaining-an-API-Key)
