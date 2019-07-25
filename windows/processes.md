# Review Running Processes

[Process Explorer](https://technet.microsoft.com/en-us/sysinternals/processexplorer.aspx) from sysinternals list all the processes running on the system hierarchically :

![processxp](../img/processxp.png)

Process Explorer should directly check the file hashes on VirusTotal, it is a good first step to identify suspicious processes. Then you should look for :
* Every program running from user directory (C:\Documents and Settings\USERNAME or C:\Users\USERNAME) is suspicious, especially the programs running from AppData
* Check for program with a name very close to a legitimate Windows process but with a small difference (lass.exe instead of lsass.exe…)
* Check for programs with a legitimate windows name (svchost.exe) outside of standard Windows directories
