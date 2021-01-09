# Onward Launcher
version 1.0
Onward version quick swap utility script
Created by Archetek and BigWing

### DISCLAIMER
This solution uses a windows batch file to rename folders and launch the Onward Steam app. You should check the contents of batch files before running on your own machine to ensure that there are no malicious commands. I have tried to comment the commands as much as possible to help usersunderstand what they do.

### CREDITS
This script just automates the process for switching Onward versions created by **BigWing** and **Ytrex**, based on work by **Monorchild**. My thanks to BigWing for extensive testing and troubleshooting.

### PREREQUISITES

- Windows Operating System
- Steam version of Onward
- Following BigWing's instructions to install Onward 1.7 and Onward 1.8 Folders
- You should have either:
  - Onward 1.7 in the **Onward** folder and Onward 1.8 in the **Onward18** folder
  - Onward 1.8 in the **Onward** folder and Onward 1.7 in the **Onward17** folder

### INSTRUCTIONS

- Optional. Open the **OnwardLauncher.bat** file in a text editor to check its contents are not malicious
- Copy the **OnwardLauncher.bat** file into the parent directory of the Onward folders (The Steam library location containing Onward, i.e. C:\Program Files (x86)\Steam\Steamapps\common)
- Run the **OnwardLauncher.bat** file
- Optional. Choose the hidden "0" option to automatically create a desktop shortcut
- Chose the "1" option to launch Onward 1.7, or the "2" option to launch Onward 1.8.
  - note: you can close the launcher immediately, but Onward may take a short time to check SteamVR is runningbefore launching into VR

### EXPLAINATION

The script prompts for the version of Onward the use wishes to launch (Options 0, 1 or 2)

- Option 1 - For launching Onward 1.7:
  - The script will check for the presence of the **Onward17** directory alongside the active **Onward** directory
  - If the Onward17 directory is found, it is assumed that the **Onward** directory contains Onward 1.8 and the **Onward17** directory contains the Onward 1.7 files
  - accordingly, it renames the active **Onward** directory as **Onward18** and the **Onward17** directory to **Onward** to switch the active version to 1.7

- Option 2 - For launching Onward 1.8:
  - The script will check for the presence of the **Onward18** directory alongside the active **Onward** directory
  - If the **Onward18** directory is found, it is assumed that the **Onward** directory contains Onward 1.7 and the **Onward18** directory contains the Onward 1.8 files
  - accordingly, it renames the active **Onward** directory as **Onward17** and the **Onward18** directory to **Onward** to switch the active version to 1.8

The script then launches Onward (App ID:496240) using the steam.exe command line (the Executable location being taken from the registry)

- Option 0 - For creating Desktop Shortcut
  - The script creates a temporary VBScript to create a Desktop Shortcut
	
### MIT LICENCE

Copyright (c) 2021 Ed Cull

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
