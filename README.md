# SIMPLE DFIR INVESTIGATION

A basic dfir investigation. This investigation was simulated and investigated on the same machine due to hardware limitations.
It simulates Stolen Credentials used to login , USB usage, simulated a harmful file(TinyRetroPad) being downloaded and then a Scheduled Task to the file being created for persistence.

## Affected Host
Computer Host: DESKTOPJD
User name: John Doe
OS:Windows 10 pro

## Simulation 

An unauthorized user gained access to John Doe’s machine. Then they connected a USB device and copied a file (sensitivedata.txt) found in the desktop folder to the USB drive and then ejected.

Then they used the chrome browser to download tinyretropad to the downloads folder.
Then they extracted the zip and run the trpad.exe. Then they created two files (file one.txt and filetwo.txt) and saved them to the downloads folder. They were both then deleted using explorer. Filetwo.txt was then removed from the recycle bin but fileone.txt was not.

Then a task was created with task schedular pointing to tinyretropad.exe to start at logon to simulate persistence. Then the user logged out and the back in to test the task schedular.Then finally logged out for the last time.


## Tools Used
USBDetective v 1.7.0 Community Edition
Timeline Explorer v2026 10.0
Registry Explorer v2026 10.0
EvtxEcmd v2026 10.0
KAPE v2026 10.0
MFT Explorer v2026 10.0