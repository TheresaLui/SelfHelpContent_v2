<properties
	pageTitle="Collect logs (Azure VPN client)"
	description="Collect logs (Azure VPN client)"
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
	articleId="1dd57e7f-59f8-47c4-a836-842bb0485ddd"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to Collect Traces for [Azure VPN client](https://docs.microsoft.com/en-us/azure/vpn-gateway/openvpn-azure-ad-client) on Windows scenario

To gather diagnostic information, collect **simultaneous** traces on the:

- Point to site Azure VPN client
- Azure VPN Gateway

During data analysis, filter traffic on the network traces according to your scenario based on the IP and ports required for your scenario. Do NOT apply traffic filters upon data collection as they may prevent you from troubleshooting properly.

## Recommended Steps

**Collecting traces on the Windows point to site client**

To troubleshoot Point to Site issues on the client side, all that is required is a Network Capture and Azure VPN client logging.

1. Start a Network capture by running **netsh trace start report=disabled capture=yes tracefile=C:\VPNclient_trace.etl** from an elevated command prompt
2. *Reproduce the connectivity issue*
3. Stop the network capture by running **netsh trace stop** from an elevated command prompt
4. Collect the Azure VPN Client logs at **%LOCALAPPDATA%\Packages\Microsoft.AzureVpn_8wekyb3d8bbwe\LocalState\LogFiles**

**Collecting traces on the Azure VPN Gateway**

1. Identify the VPN gateway in ASC.
2. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
3. Choose the duration in minutes and click **Run**
1. *Reproduce the connectivity issue*
1. After the diagnostic operation is completed, you can download the zip file containing the traces
1. The most relevant file for point to site connection is the **networktrace.etl** (packet capture on the gateway side)
1. Other than a live trace, remember than text-based logging is available on Jarvis at the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B). Data is normally filled in Jarvis 5-10 minutes after the repro.

If you identify a specific error from any the logs, re-run the TSG by selecting "The customer has provided an error".

Engage a TA shall you require help reviewing any of the collected logs.
