# Monitor Network Traffic

Monitoring network traffic from a phone is one of the best way to identify malicious activity without interacting with the mobile phone.

## Monitor Network Activity from a Wifi Router

One of the easiest way to monitor the network traffic from your phone is to record the traffic directly from a WiFi router used by your mobile phone. Depending on your WiFi router, it may be possible to record traffic directly from it (using a tool like [tcpdump](https://www.tcpdump.org/)).

If your WiFi router does not support this option, you can easily build a router using  a [Raspberry Pi](https://www.raspberrypi.org/) an the software [RaspAP](https://raspap.com/) (see [here](https://howtoraspberrypi.com/create-a-wi-fi-hotspot-in-less-than-10-minutes-with-pi-raspberry/) for a tutorial on how to install it).

Once installed, you can connect to the router using ssh and start capturing the traffic using [tcpdump](https://www.tcpdump.org/). Then connect your mobile phone to this wifi network and record the traffic to 30 minutes to one hour.

After the end of the recording, you can downloading the pcap file on your computer and review the network traffic using [WireShark](https://www.wireshark.org/). Check especially the following elements :
* Connections to IP addresses without DNS requests
* Connections to domains that are not listed in [Alexa Top lists](https://www.alexa.com/siteinfo)
* Connections on ports other than 80 and 443

## Use CivicSphere Emergency VPN

The [Civil Sphere Project](https://www.civilsphereproject.org/what-we-do), an organisation developed from the [Stratosphere Research Laboratory](https://www.stratosphereips.org/) at the Czech Technical University in Prague, offers an [Emergency VPN](https://www.civilsphereproject.org/emergency-vpn) as a service to identify compromised devices.

The Emergency VPN service allows to analyze and identify suspicious traffic from a mobile device for journalists and NGOs. [On demand](https://www.civilsphereproject.org/get-started), the Civil Sphere team will send you credentials to log-in to their VPN with your phone. While using their VPN, they will record all the traffic coming out of your phone for a maximum of three days. At the end of the recording, they will analyze the traffic using automated and manual techniques in order to identify malicious activity or insecurities of applications used, and provide you the result of the analysis by email.

![vpn](../img/emergencyvpn.png)

One of the limitation of this technique is that you have to provide network traffic from your mobile phone to a third party organisation (Civil Sphere), you can [contact them](https://www.civilsphereproject.org/get-started) to have more information about how this data is stored and used.

Check [their website](https://www.civilsphereproject.org/emergency-vpn) for more information.




