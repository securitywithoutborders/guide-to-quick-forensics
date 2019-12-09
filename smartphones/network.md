# Monitor Network Traffic

Monitoring network traffic from a phone is one of the best way to identify malicious activity without interacting with the mobile phone hence bypassing any mechanism the malware may have developed to bypass detection. But it requires an external tool to record the traffic and some network knowledge to identify suspicious traffic.

## Monitor Network Activity from a Wifi Router

One way to monitor the network traffic from your phone is to record the traffic directly from a WiFi router used by your mobile phone. Depending on your WiFi router, it may be possible to record traffic directly from it (using a tool like [tcpdump](https://www.tcpdump.org/)).

If you cannot record traffic using your actual WiFi router, you can easily build a router using a [Raspberry Pi](https://www.raspberrypi.org/) and the [RaspAP](https://raspap.com/) software (see [here](https://howtoraspberrypi.com/create-a-wi-fi-hotspot-in-less-than-10-minutes-with-pi-raspberry/) for a tutorial on how to install it).

Once your router is installed, you can connect to it using ssh and start capturing the traffic using [tcpdump](https://www.tcpdump.org/). Then connect the mobile phone you want to test to this wifi network and record the traffic for 30 minutes to one hour.

After the end of the capture, download the pcap file on your computer and review the network traffic using [WireShark](https://www.wireshark.org/). Check especially the following elements :
* Connections to IP addresses without DNS requests
* Connections to domains that are not listed in [Alexa Top lists](https://www.alexa.com/siteinfo)
* Connections on ports other than 80 and 443

If you find any suspicious traffic to an IP address or domain, you can use the following tools to get more information on it :
* [CentralOps](https://centralops.net/co/) allows to see the owner of an IP or the whois of a domain (does not require an account)
* [RiskIQ](https://community.riskiq.com/home) allows to see the DNS history and has many indications about malicious IPs and domains (requires an account, limited number of queries with a free account)
* [AlienVault OTX](https://otx.alienvault.com/) is a large database of malicious indicators, you can search for this IP or domain in it to see if there is known malicious activity from it (requires an account, free)

## Use Civil Sphere Emergency VPN

The [Civil Sphere Project](https://www.civilsphereproject.org/what-we-do), an organisation born from the [Stratosphere Research Laboratory](https://www.stratosphereips.org/) at the Czech Technical University in Prague, offers an [Emergency VPN](https://www.civilsphereproject.org/emergency-vpn) service to identify compromised devices.

The Emergency VPN service allows to analyze and identify suspicious traffic from a mobile device used by journalists and NGOs. [On demand](https://www.civilsphereproject.org/get-started), the Civil Sphere team will send you credentials to log-in to their VPN with your phone. While using their VPN, they will record all the traffic coming out of your phone for a maximum of three days. At the end of the recording, they will analyze the traffic using automated and manual techniques in order to identify malicious activity or security issues in the applications running on your phone, and send you the result of this analysis by email.

<center>
<img src="../img/emergencyvpn.png" style="max-width:40%">
</center>

One of the limitation of this technique is that you have to provide network traffic from your mobile phone to a third party organisation (Civil Sphere), you can [contact them](https://www.civilsphereproject.org/get-started) to have more information about how this data is stored and used. The advantage of this solution is that you can rely on them to analyze the network traffic, which can be a complex and time-consuming process.

Check [their website](https://www.civilsphereproject.org/emergency-vpn) for more information.
