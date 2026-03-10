# AndroXploit - exploit open ADB ports

## About the tool
This tool is designed for post-exploitation of open Android Debug Bridge (ADB) ports - inspired by the "Ghost framework". The tool is still under development and may introduce new functionalities in future. Stay updated with this repo to get it sooner.


## Installation
- Make sure you have ADB utility installed in your linux system.
- Get the binary from the release section of this repository.
- Give it executable permission with `chmod +x androxsploit`
- Now you can run the binary with `./androxsploit` as usual. Enjoy!


### Available commands:
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

Information gathering commands:
---------
[+] getbat - shows the battery information
[+] accounts - extracts the accounts associated with the target device
[+] contacts - extracts phone contacts if available
[+] connected_wifi - shows the connected wifi SSID
[+] getinfo - shows the device model
[+] printenv - extracts the environment variables
[+] isroot - checks if the device is rooted.
[+] imginfo - shows information of all the image in the target device
[+] lockstat - checks if the screen is currently locked or not

Active user interaction commands:
---------
[+] type - simulates keyboard typing of given string on the target devices [generally, input field needs to be focused, on some devices it may trigger google search input]
[+] pin - tries to unlock the screen using given PIN [if PIN locked]
[+] launch - extracts & starts the main activity of a given package [basically launches the app]
[+] clrecent - clears out all the running applications in "Recents" tab & exitting the currently open app as well. You can ignore the errors it throws when trying to remove non-standars stacks.

File handling commands:
---------
[+] lsxpacks - list all the third party apps installed
[+] lspacks - list all the packages
[+] pull - download files or directories from the device into your local system
[+] push - upload files to the target device from your local system
[+] install - upload files to the target device from your local system [use -g to grant all runtime perms automatically]
[+] filestruct - prints the file-system structure under /sdcard
[+] locate - extracts the geolocation of the device if enabled


```
