# Checking Devices Remotely

In this time of almost worldwide confinement, we are adding here a few steps that may help to check for potentially compromised devices remotely. It includes for now only solutions for Windows and Mac OS computers using [Teamviewer](https://www.teamviewer.com/en/) and [Chrome Remote Desktop](https://remotedesktop.google.com/), as we do not have yet any satisfying solution for smartphones (any suggestion [is welcome](https://github.com/securitywithoutborders/guide-to-quick-forensics/issues)).

## Limitations of Remote Forensic

### The Problem of Trust

With any remote desktop solution relying on a third party platform, there is an important question of trust. When you install such a remote desktop software, you have to know that the company developing the solution can use the software to access your computer but also can record any interaction you have through their solution. It is thus very important use a solution that you trust based on your threat model.

In this guide we use two software :

* [Teamviewer](https://www.teamviewer.com/en/) is a developed by TeamViewer AG, a German company based in Göppingen.
* [Chrome Remote Desktop](https://remotedesktop.google.com/) is developed by Google and is integrated in the Google ecosystem (which requires you to use Google accounts).

Teamviewer had several security issues in the past, the FireEye company claimed that it was breached by a [Chinese state-sponsored group in October 2019](https://www.securitynewspaper.com/2019/10/14/fireeye-confirms-that-apt14-group-hacked-teamviewer-attackers-would-have-accessed-billions-of-devices/). We tend to trust more Google for its security, but depending on your threat model, Teamviewer may be a better option. We are using Teamviewer for Windows here because Chrome Remote Desktop does not support well Mac OS yet (no file sharing).

### The Problem of Needing Online Access

Another issue with checking devices remotely is that you need the device to have access to Internet. As [explained before](safety.md), this can lead to some risks for the user. If the device is actually compromised and monitored remotely, the operators may identify that the user is receiving technical support and it may cause retaliation against the person you are trying to support.

You should make sure to address that risk before doing any remote support.

## Some Information on the Process

In order to schedule the check of a device remotely, you need to exchange beforehand with the person to let them know that :

* They will have to install a remote desktop software before
* They will have to stay in front of the computer during the check to enter the admin password (a check often last between 30 minutes and an hour)
* They will have to remove the remote desktop software after

Please keep in mind that [trust](trust.md) is a key part of any security support, so you should make sure that the process is clear for the person you are supporting and that they consent to it.

