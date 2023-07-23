ConnectWise :  It is a remote access and remote control software
<br>

| S.No | Artifact            | Source   | Comment |
|:-----:|:----------------|:---------|:--------------------|
|1  | %ProgramFiles(x86)%\ScreenConnect Client (<random>)\*  | Installation Path  | --  |
|2  | Check for event ID 7045 and try to search for keyword "ScreenConnect"  | Security.evtx  | -- |
|3  | Check for event ID 1033 and try to search for keyword "ScreenConnect" (MSI Installer) | Application.evtx  | --  |
|4  | Check for event ID 11707 and try to search for keyword "ScreenConnect" (Installation Completed Successfully)  | Application.evtx  | --  |
|5  | Check for event ID 0 and try to search for keyword "Cloud Account Administrator Connected" | Application.evtx  | --  |
|6  | Check for event ID 0 and try to search for keyword "Cloud Account Administrator Disconnected" | Application.evtx  | --  |
|7  | Check for event ID 0 and try to search for keyword "Transferred files with action 'Transfer'" | Application.evtx  | The event logs are recorded each times files are sent from attacker to victim |
|8  | Check for event ID 0 and try to search for keyword "Executed command of length" | Application.evtx| --|
|9  | Check for event ID 400,403,600 & try to search for keyword "ScreenConnect" | Windows PowerShell.evtx| --|
|10  | Check for event ID 4104 & try to search for keyword "ScreenConnect" | Microsoft-Windows-PowerShell/Operational.evtx |If script block logging is enabled, specific process will be listed|