# Review Running Processes

A computer infected with spyware should have some malicious processes running at all times, monitoring the system and collecting data to be transmitted to the [Command & Control server](https://securitywithoutborders.org/resources/digital-security-glossary.html#cnc) of the attackers. Therefore, another required step in triaging a suspected MacOS computer is to extract the list of running processes and find if any of them display suspicious characteristics

The best tool to do so is [TaskExplorer](https://objective-see.com/products/taskexplorer.html) developed by Objective-See. You first need to download the program from [its official page](https://objective-see.com/products/taskexplorer.html), unzip the archive containing the program  (double-clicking on it should work in most cases) and double-click on the TaskExplorer program to launch it. On startup, it will ask for your password in order to get administrator privileges to list all the processes running.

![](../img/taskexplorer3.png)

Before proceeding with this check, it is advisable that you close all visible running applications, in order to reduce the outputs of the tools you will run to the bare minimum.

### 1. Verify Image Signature

Similarly to KnockKnock, TaskExplorer verifies the signature of applications running. This information is shown with a loc icon near the Application name, a green closed lock ![](../img/signedApple.png) means that an application belong to Apple, a black closed lock ![](../img/signed.png) means that it is a Non-Apple signed application and an open orange lock ![](../img/unsigned.png) means that the application is not signed.

You can filter tasks to see only non-signed applications by writing `#unsigned` in the filtering bar and hit enter :

![](../img/taskexplorer2.png)

### 2. Check for Suspicious Application Name and Path

As in the startup section, it is interesting to check for any application that has a suspicious name and path. The name of the application can be faked but in some cases, malware are using either spoofed name with typos (such as `Crhome`) or random strings.

The path of the application gives indication on where the application is running from. Any application running from a location other than `/Library` or `/Applications` should be investigated further.

To avoid checking legitimate applications signed by Apple, you can filter the tasks with the hashtag `#nonapple` in the fitering bar :

![](../img/taskexplorer4.png)

### 3. Looking up Programs on VirusTotal

Similarly to [Autoruns](autoruns.md) section, TaskExplorer also checks file fingerprint on VirusTotal. On the right of each task running, you will see two numbers representing first the number of antiviruses that identified this file as malicious and then the total number of antiviruses tested. An question mark will appear if this program is not known by VirusTotal.

![](../img/taskexplorer1.png)

You should investigate further any task identified by at least one antivirus as malicious or not known by VirusTotal.

**Please note:** the same considerations and warnings explained in the [previous section](autoruns.md) apply here too. Make sure to read them before proceeding.
