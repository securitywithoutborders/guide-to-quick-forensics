# Extract Data for Further Analysis

If you have not found anything suspicious on the system but want to investigate further without the system, it is possible to collect interesting forensic data in order to analyze them later using [AutoMacTC](https://www.crowdstrike.com/blog/automating-mac-forensic-triage/)

**This program can extract some private information (such as browser history), keep that in mind while using it.**

## Launching AutoMacTC

You first need to download AutoMacTC from [the Github repository](https://github.com/CrowdStrike/automactc/archive/master.zip) and extract it.

Then you have to launch a terminal, from the menu > `Other` > `Terminal`. To run the program you need to know the path of the extracted AutoMacTC code and run `sudo python <PATH>/automactc-master/automactc.py -m all`.

![](../img/automactc.png)

Running this command with the argument `-m all` will extract all the data available. It is also possible to extract more specific data by passing the name of a specific module. Here is the list of modules from [AutoMacTC documentation](https://www.crowdstrike.com/blog/automating-mac-forensic-triage/) :
* pslist : current process list at time of AutoMacTC run
* lsof : current file handles open at time of AutoMacTC run
* netstat : current network connections at time of AutoMacTC run
* asl : parsed Apple System Log (.asl) files
* autoruns : parsing of various persistence locations and plists
* bash : parsing `bash/.*_history` files for all users
* chrome : parsing chrome visit history and download history
* coreanalytics : parsing program execution evidence produced by Apple diagnostics
* dirlist : list of files and directories across the disk
* firefox : parsing firefox visit history and download history
* installhistory : parsing program installation history
* mru : parsing SFL and MRU plist files
* quarantines : parsing QuarantineEventsV2 database
* quicklook : parsing Quicklooks database
* safari : parsing safari visit history and download history
* spotlight : parsing user spotlight top searches
* ssh : parsing known_hosts and authorized_keys files for each user
* syslog : parsing system.log files
* systeminfo : basic system identification, such as current IP address, serial no, hostname
* users : listing present and deleted users on the system
* utmpx : listing user sessions on terminals

## Data Extracted

All the data extracted are saved in an archive name `automactc-output,<computername>,<ipaddress>,<date>.tar.gz`. It contains csv files with results for all modules executed.
