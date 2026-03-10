# AndroXploit - exploit open ADB ports

```code
           .            .           
            \          /                                                                                            
         ____\________/____                                                                                         
        /                  \                                                                                        
       /    ██        ██    \                                                                                       
      |     ██        ██     |                                                                                      
      |         ____         |                                                                                      
      |______________________|                                                                                      
    _              _         __  __      _       _ _   
   / \   _ __   __| |_ __ ___\ \/ /_ __ | | ___ (_) |_ 
  / _ \ | '_ \ / _` | '__/ _ \\  /| '_ \| |/ _ \| | __|
 / ___ \| | | | (_| | | | (_) /  \| |_) | | (_) | | |_ 
/_/   \_\_| |_|\__,_|_|  \___/_/\_\ .__/|_|\___/|_|\__|
                                  |_|                  
A project by MR_Prey3r - for exploiting open ADB
https://github.com/MR-Prey3r/androxploit 
```


## DESCRIPTION
AndroXploit is a lightweight yet powerful shell-based framework for interacting with Android devices via ADB. Inspired by the Ghost Framework, this tool streamlines reconnaissance, activity tracking, and device manipulation into a single, automated interface.

Designed for security researchers and developers who need a "surgical" approach for post-exploitation of open Android Debug Bridge (ADB) ports. Helpful for penetration testing as well as android debugging. The idea is inspired by - Metasploit & "Ghost framework". The tool is still under development and may introduce new functionalities in future. Stay updated with this repo to get it sooner. If you encounter any issue with the tool, feel free to initiate an issue on this repository.


## 🔥 KEY FEATURES
- Deep Recon: Extract a whole bunch of system information to get advantage in the attackflow.
- Activity/Package Filtering: View "Standard" user apps & their activities while ignoring system noise.
- Direct remote shell access to the device
- Made easier execution for longer ADB commands & filtering annoying noisy output
- *More features to come!*

## INSTALLATION
- Make sure you have ADB utility installed in your linux system.
- Get the binary from the [release](https://github.com/MR-Prey3r/AndroXploit/releases) section of this repository.
- Give it executable permission with `chmod +x androxsploit`
- Now you can run the binary with `./androxsploit` as usual. Enjoy!


### USAGE / Available commands:
```code
Commands:
-------------------- 
[+] help - displays the help
[+] clear - clears the screen
[+] exit - to exit the tool prompt
[+] connect - connects to the specified host at port 5555 by default. Example: 'connect 10.20.30.40'
[+] list - lists the connected devices
[+] disconnect - disconnects a connected device. Example 'disconnect 10.20.30.40'
[+] ss - captures a screenshot of the device. Example: 'ss output.png'
[+] getsh - opens you a shell on the target device
[+] clrsh - tries clearing the history of executed commands in the shell of the target device

Deep recon commands:
---------
[+] getbat - shows the battery information
[+] accounts - extracts the accounts associated with the target device
[+] contacts - extracts phone contacts if available
[+] connected_wifi - shows the currently connected wifi SSID
[+] getall_wifi - shows all the network(wifi/hostpot) SSID the device was ever connected to
[+] getinfo - shows the device model
[+] printenv - extracts the environment variables
[+] isroot - checks if the device is rooted.
[+] imginfo - shows information of all the image in the target device
[+] lockstatus - checks if the screen is currently locked or not
[+] focused - shows the package name & its activity currently the device has on the screen
[+] custom_words - shows the custom words the user has typed (often contains names, slang, or partial passwords).
[+] keycodes - lists all the available keycodes/keyevents in the device
[+] wireshark - opens device tcpdump network logs in wireshark for better monitoring (may require root access)
[+] readclipboard - reads the clipboard data if available (may require root access)
[+] screenrecord - records screen & pulls the record data into your local machine (default time limit is set to maximum [60s]). If the screen's locked, you may get e blank file

Active user interaction commands:
---------
[+] type - simulates keyboard typing of given string on the target devices [generally, input field needs to be focused, on some devices it may trigger google search input]
[+] pin - tries to unlock the screen using given PIN [if PIN locked]
[+] launch - extracts & starts the main activity of a given package [basically launches the app]
[+] clrecent - clears out all the running applications in "Recents" tab & exitting the currently open app as well. You can ignore the errors it throws when trying to remove non-standars stacks.
[+] tap - taps/clicks on the given Y, X coordinates. [Usage: tap Y X]
[+] openurl - opens a given url
[+] setmediavol - sets media volume to the given value (min:0, max: 15)

File handling commands:
---------
[+] lsxapk - lists all the third party apps installed. Pass "save" argument to save the list in a file [Example: lsxapk save]
[+] lsapk - lists all the apps including system apps. Pass "save" argument to save the list in a file [Example: lsapk save]
[+] activities - lists all the activities of all packages
[+] pull - download files or directories from the device into your local system
[+] push - upload files to the target device from your local system
[+] install - upload files to the target device from your local system [use -g to grant all runtime perms automatically]
[+] filestruct - prints the file-system structure under /sdcard
[+] locate - extracts the geolocation of the device if enabled

```

## ⚠️ DISCLAIMER
This tool is solely for educational and authorized security testing purposes only. The author is not responsible for any misuse or damage caused by this script. Be responsible, stay sharp, smart & ethical!



## ⚖️ LICENSE & CREDITS

This project is licensed under the MIT License.

Original Author: MR_Prey3r

Inspiration: Inspired by the legendary Metasploit & Ghost Framework.

Note: If you modify or improve this script, inspiring credit is appreciated! (This shell script might go open-source in future)

