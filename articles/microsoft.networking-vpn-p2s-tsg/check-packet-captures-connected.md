<properties
	pageTitle="Collect Packet Captures (Connected)"
	description="Collect Packet Captures (Connected)"
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
	articleId="44cfafa1-e32c-4719-8c88-a4f718fbc838"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Collect Packet Captures in 'Connected but can't reach destination' scenario

If the point to site VPN is connected, but the client can't reach the destination, the issue is one of the following:

1. The client doesn't send the traffic into the VPN tunnel.
2. The gateway fails to forward the traffic towards destination
3. There is an issue in the path between gateway and destination

Packet captures collected at the same time on all three places will help identify the issue.
To gather diagnostic information, collect **simultaneous** traces on the:

- Point to site VPN client
- Azure VPN Gateway
- destination Azure VM

During data analysis, filter traffic on the network traces according to your scenario based on the IP and ports required for your scenario. Do NOT apply traffic filters upon data collection as they may prevent you from troubleshooting properly.


## Recommended Steps

### Collecting traces on Point to site client

If Windows:
* Start a Network capture by running **netsh trace start report=disabled capture=yes tracefile=C:\VPNclient_trace.etl** from an elevated command prompt
* *Reproduce the connectivity issue*
* Stop the network capture by running **netsh trace stop** from an elevated command prompt

If Linux:
* Start a Network capture by running **tcpdump -s 0 -i eth0 -w VPNclient_trace.pcap**
* *Reproduce the connectivity issue*
* Stop the network capture by pressing **CTRL+C**

If Mac OS:
* You can install Wireshark  or similar tool to gather a packet cature from the Mac client. Else you can follow Apple guidelines to use tcpdump via command line. https://developer.apple.com/documentation/network/recording_a_packet_trace 

### Collecting traces on the Azure VPN Gateway

1. Identify the VPN gateway in ASC.
1. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
1. Choose the duration in minutes and click **Run**
1. *Reproduce the connectivity issue*
1. After the diagnostic operation is completed, you can download the zip file containing the traces
1. The most relevant files for point to site connection are the **networktrace.etl** (packet capture on the gateway side) and the **TunnelInnerPacketTrace.etl** that captures traffic on the inner interface of the gateway.
1. Read more about inner and outer packet captures on the [wiki](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/134103/Azure-Gateway-Diagnostics?anchor=understanding-inner-and-outer-packet-captures).

### Collecting traces on the destination Azure VM

***If Windows***

1. Start a Network capture by running **netsh trace start report=disabled capture=yes tracefile=C:\azureVM_trace.etl** from an elevated command prompt
1. *Reproduce the connectivity issue*
1. Stop the network capture by running **netsh trace stop** from an elevated command prompt

***If Linux***

1. Start a Network capture by running **tcpdump -s 0 -i eth0 -w azureVM_trace.pcap**
1. *Reproduce the connectivity issue*
1. Stop the network capture by pressing **CTRL+C**

Engage a TA shall you require help reviewing any of the collected logs.
