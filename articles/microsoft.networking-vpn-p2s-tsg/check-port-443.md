<properties
	pageTitle="Check Port 443"
	description="Check Port 443"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="4c87b9e1-f69a-4589-a697-aeb2261a2fa2"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check if gateway is listening on port 443

Easiest test is to perform a TCP ping on port 443, for example using PSPing.

1. Go to ASC > Resource Explorer and select the VPN gateway
2. Copy the Public IP address of the gateway labelled as **Gateway VIP**
3. Open a command prompt window and run the following command **psping <Gateway VIP>:443**

Example:

~~~
C:\Users\administrator>psping 40.115.164.54:443
PsPing v2.01 - PsPing - ping, latency, bandwidth measurement utility
Copyright (C) 2012-2014 Mark Russinovich
Sysinternals - www.sysinternals.com

TCP connect to 40.115.164.54:443:
5 iterations (warmup 1) connecting test:
Connecting to 40.115.164.54:443 (warmup): 224.58ms
Connecting to 40.115.164.54:443: 221.00ms
Connecting to 40.115.164.54:443: 218.83ms
Connecting to 40.115.164.54:443: 219.18ms
Connecting to 40.115.164.54:443: 221.24ms

TCP connect statistics for 40.115.164.54:443:
Sent = 4, Received = 4, Lost = 0 (0% loss),
Minimum = 218.83ms, Maximum = 221.24ms, Average = 220.06ms
~~~

**Important: the gateway might be correctly listening on port 8081 as per previous steps (meaning the gateway is healthy) but it might fail to respond on port 443.**

If OpenVPN is enabled and Gateway is not responding, we are facing an issue on the Gateway.
