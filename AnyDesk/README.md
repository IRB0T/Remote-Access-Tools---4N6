AnyDesk :  It is a remote access and remote control software
<br>

| S.No | Artifact            | Source   | Comment |
|:-----:|:----------------|:---------|:--------------------|
|1  | AnyDesk.exe --install “%ProgramFiles(x86)%AnyDesk” --start-with-win --silent   | Command  | Installation String  |
|2  | echo &lt;my_password&gt; \| anydesk.exe --set-password | Command  | Password for remote connection can be set using command line  |
|3  | %ProgramFiles(x86)%\AnyDesk\  | Installation Path  | -  |
|4  | %ProgramFiles%\AnyDesk\  | Installation Path  | -  |
|5  | %ProgramData%\AnyDesk\ad_svc.trace  | Log File Path  | -  |
|6  | %AppData%\AnyDesk\ad.trace  | Log File Path  | -  |
|7  | %ProgramData%\AnyDesk\system.conf  | Log File Path  | -  |
|8  | %ProgramData%\AnyDesk\service.conf  | Log File Path  | -  |
|9  | %AppData%\AnyDesk\system.conf  | Log File Path  | -  |
|10  | %AppData%\AnyDesk\service.conf  | Log File Path  | -  |
|11  | %ProgramData%\AnyDesk\connection_trace.txt  | Log File Path  | -  |
|12  | %AppData%\AnyDesk\connection_trace.txt  | Log File Path  | -  |
|13  | "anynet.any_socket - Accepting from"  | Keyword  | Search given Keyword in ad.trace file to get AnyDesk ID of Remote Machine  |
|14  | "anynet.any_socket - Logged in from"  | Keyword  | Search given Keyword in ad.trace file to get IP address of Remote Machine  |
|15 | "app.local_file_transfer - Download Started"  | Keyword  | Search given Keyword in ad.trace file to traces of file uploaded from remote machine  |
|16  | "app.prepare_task - Preparing files in"  | Keyword  | Search given Keyword in ad.trace file to traces of file Download from client machine  |
|17 | "app.deleter - Deleting"  | Keyword  | Search given Keyword in ad.trace file to traces of file deletion  |
|18  | gcapi.dd  | File  | If AnyDesk is running in standalone mode then you will see traces of this file |


Knowledge Base </br>
In "connection_trace.txt" file you will get following things</br>
<ol>
<li>"Data/Time of remote access"</li>
<li>Authentication Type:</li>
<ol>
<li>User: Indicate connection was accepted using GUI on client Machine</li>
<li>Passwd: Indicate connection was established by providing Password</li>
<li>Token: Indicate connection was established by stored Password</li>
</ol>
<li>AnyDesk ID of Source Machine</li>
</ol>