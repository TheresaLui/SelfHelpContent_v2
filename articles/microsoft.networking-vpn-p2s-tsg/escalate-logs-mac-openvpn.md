<properties
	pageTitle="Collect Logs (MAC OpenVPN)"
	description="Collect Logs (MAC OpenVPN)"
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
	articleId="0a69ff1c-eec8-4a16-ad9e-100f07833357"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to Collect Traces for MAC OpenVPN client scenario

To gather diagnostic information, collect **simultaneous** traces on the:

- Mac Point to site VPN client
- Azure VPN Gateway

During data analysis, filter traffic on the network traces according to your scenario based on the IP and ports required for your scenario. Do NOT apply traffic filters upon data collection as they may prevent you from troubleshooting properly.

## Recommended Steps

**Collecting traces on the Mac point to site OpenVPNclient**

1. Install [Wireshark](https://www.wireshark.org/download.html) or similar tool to gather a packet capture from the Mac client.
Else you can follow Apple guidelines to use tcpdump via command line.
https://developer.apple.com/documentation/network/recording_a_packet_trace
2. Collect the OpenVPN logs normally located at */Library/Application Support/OpenVPN/log/openvpn_(unique_name).log*.

**Collecting traces on the Azure VPN Gateway**

1. Identify the VPN gateway in ASC.
2. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
3. Choose the duration in minutes and click **Run**
4. Reproduce the connectivity issue
5. After the diagnostic operation is completed, you can download the zip file containing the traces
6. The most relevant file for point to site connection is the **networktrace.etl** (packet capture on the gateway side)
7. Other than a live trace, remember than text-based OpenVPN logging is available on Jarvis at the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B). Data is normally filled in Jarvis 5-10 minutes after the repro.

If you identify a specific error from any the logs, re-run the TSG by selecting "The customer has provided an error".

Engage a TA shall you require help reviewing any of the collected logs.
