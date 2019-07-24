# Methodology

The methodology for doing quick forensics can be quite ad-hoc, and eventually with time you will develop your own. This guide should help in this process. Generally, when trying to triage a possible infection, you will like for any anomaly that you are able to identify on the device. Such anomalies, for example, can be:

1. Applications and processes running on the device that you and the owner of the device do not recognize. Applications and processes that show some unusual characteristics, such as suspicious names and file locations, or attempts at hiding.
2. Because spyware normally would want to be able to survive a shutdown of the device, you will look for applications which maintain persistence over the device and are therefore registered for automatic execution at startup.
3. Suspicious network connections to infrastructure and services that you and the owner of the device do not recognize.

While it is not possible to compile an exhaustive checklist of precise anomalies to look out for, the process of developing a robust quick forensics methodology will require *training your eye*, by inspecting as many devices you can get your hands. Eventually, you will start recognizing patterns across various operating systems, and become more rapid and efficient at discarding legitimate applications and spotting those that stand out. It takes practice.

## Considerations on legal litigation

When it comes to legal litigation, for example against the attacker or a company who provided aid to the attacker, there are certain forensic procedures that should normally be respected.
If you think there are elements in the case you are working on that might lead to a legal investigation, you should consult with local advisors and perhaps seek instead the assistance of an accredited forensics firm.
