# Optional : Check for Indicators of Stalkerware Installation

Stalkerwares are malicious applications used in the context of Intimate Partner Violence. One of the difference with classic android malware is that they are installed through a physical access to the smartphone. Because of this, the installation requires some changes on the Android system that can often be identified later on.

## Check if Installation from Unknown Sources is Authorized

Stalkerware applications are installed directly from the application file (APK), which is by default forbidden by Android. To install the application, the person needs to allow the installation from Unknown Sources.

Before Android 8 "Oreo", this feature was enabled for the entire phone. If you have a phone before Android 8, go to **Settings > Security** and check if **Unknown Sources** is enabled.

<center>
<img src="../img/unknown_sources.png" style="max-width:40%">
</center>

After Android 8, this feature is enabled per application. Go to **Settings > Security > Install unknown apps** to see the list of applications allowed to install untrusted applications.

<center>
<img src="../img/unknown_sources2.png" style="max-width:40%">
</center>

Any application in this list is suspicious, especially browsers and file managers.

## Check if Google Play Protect is Disabled

Google Play Protect is an automated detection of malicious applications developed and maintained by Google as part of their Google Play Services. This feature often needs to be disabled during the installation of a stalkerware application because it can detect the malicious app.

To check this setting, you should have to go to **Settings > Security > Scan Devices for Security Threats** or **Settings > Security > Google Play Protect** depending on your version of Android.

<center>
<img src="../img/androidscan.png" style="max-width:40%">
</center>

## Check if the Phone is Rooted

A stalkerware application often requires a rooted phone to have access to more data. Follow the recommendations of [this other part of this guide](root.md) to check if the phone is rooted.
