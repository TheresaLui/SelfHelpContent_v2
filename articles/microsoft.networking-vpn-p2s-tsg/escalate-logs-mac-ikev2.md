<properties
	pageTitle="Collect Logs (Mac IKEv2)"
	description="Collect Logs (Mac IKEv2)"
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
	articleId="6a16d9e7-7a06-491a-b14f-8d7813bab36c" 
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Collect Traces for MAC IKEv2 client scenario

To gather diagnostic information, collect **simultaneous** traces on the:

- Mac Point to site VPN client
- Azure VPN Gateway

During data analysis, filter traffic on the network traces according to your scenario based on the IP and ports required for your scenario. Do NOT apply traffic filters upon data collection as they may prevent you from troubleshooting properly.

**Collecting traces on the Mac point to site IKEv2 client**

1. Install [Wireshark](https://www.wireshark.org/download.html) or similar tool to gather a packet capture from the Mac client. Else you can follow [Apple guidelines](https://developer.apple.com/documentation/network/recording_a_packet_trace) to use tcpdump via command line.


**Collecting traces on the Azure VPN Gateway**

1. Identify the VPN gateway in ASC.
2. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
3. Choose the duration in minutes and click **Run**
4. *Reproduce the connectivity issue*
5. After the diagnostic operation is completed, you can download the zip file containing the traces
6. The most relevant file for point to site connection is the **networktrace.etl** (packet capture on the gateway side)
7. Other than a live trace, remember than text based IKEv2 logging is available on Jarvis at the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B) and [IkeLogsTable](https://jarvis-west.dc.ad.msft.net/A5B239BD). Data is normally filled in Jarvis 5-10 minutes after the repro.

If you identify a specific error from any the logs, re-run the TSG by selecting "The customer has provided an error".

Engage a TA shall you require help reviewing any of the collected logs.
