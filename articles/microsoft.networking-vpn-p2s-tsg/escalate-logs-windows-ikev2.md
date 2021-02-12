<properties
	pageTitle="Collect logs (Windows IKEv2)"
	description="Collect logs (Windows IKEv2)"
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
	articleId="b40f09a7-b435-4d43-84d1-47a55885e8a5"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to Collect Traces for Windows IKEv2 client scenario

To gather diagnostic information, collect **simultaneous** traces on the:

- Point to site VPN client
- Azure VPN Gateway

During data analysis, filter traffic on the network traces according to your scenario based on the IP and ports required for your scenario. Do NOT apply traffic filters upon data collection as they may prevent you from troubleshooting properly.

## Recommended Steps

**Collecting traces on the Windows point to site IKEv2 client**

To troubleshoot Point to Site issues on the client side, all that is required is a Network Capture and WFPdiag logging.

1. Start WFPdiag tracing by running **netsh wfp capture start**
1. Start a Network capture by running **netsh trace start report=disabled capture=yes tracefile=c:\VPNclient_trace.etl** from an elevated command prompt
1. *Reproduce the connectivity issue*
1. Stop the network capture by running **netsh trace stop** from an elevated command prompt
1. Stop the WFPdiag tracing by running **netsh wfp capture stop**. The file is normally saved at the **C:\Windows\System32\WFPdiag.etl** path

## Collecting traces on the Azure VPN Gateway

1. Identify the VPN gateway in ASC.
1. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
1. Choose the duration in minutes and click **Run**
1. *Reproduce the connectivity issue*
1. After the diagnostic operation is completed, you can download the zip file containing the traces
1. The most relevant file for point to site connection is the **networktrace.etl** (packet capture on the gateway side)
1. Other than a live trace, remember than text-based IKEv2 logging is available on Jarvis at the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B) and [IkeLogsTable](https://jarvis-west.dc.ad.msft.net/A5B239BD). Data is normally filled in Jarvis 5-10 minutes after the repro.

If you identify a specific error from any the logs, re-run the TSG by selecting "The customer has provided an error".

Engage a TA shall you require help reviewing any of the collected logs.
