<properties
	pageTitle="Collect logs (Windows SSTP)"
	description="Collect logs (Windows SSTP)"
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
	articleId="c929d9ec-34b0-4655-8b5f-d700622420a1"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to Collect Traces for Windows SSTP client scenario

To gather diagnostic information, collect **simultaneous** traces on the:

- Point to site VPN client
- Azure VPN Gateway

During data analysis, filter traffic on the network traces according to your scenario based on the IP and ports required for your scenario. Do NOT apply traffic filters upon data collection as they may prevent you from troubleshooting properly.

## Recommended Steps

**Collecting traces on the Windows point to site SSTP client**

To troubleshoot Point to Site issues on the client side, all that is required is a Network Capture and RAS logging.

1. Start RAS tracing by running **netsh ras set tracing * enable**
1. Start a Network capture by running **netsh trace start report=disabled capture=yes tracefile=C:\VPNclient_trace.etl** from an elevated command prompt
1. *Reproduce the connectivity issue*
1. Stop the network capture by running **netsh trace stop** from an elevated command prompt
1. Stop the RAS tracing by running **netsh ras set tracing * disable**. Logs will be found in *C:\Windows\Tracing* folder.

**Collecting traces on the Azure VPN Gateway**

1. Identify the VPN gateway in ASC.
1. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
1. Choose the duration in minutes and click **Run**
1. *Reproduce the connectivity issue*
1. After the diagnostic operation is completed, you can download the zip file containing the traces
1. The most relevant files for point to site connection are the **networktrace.etl** (packet capture on the gateway side) and the **RRAS_logs** zip file that will only be generated if SSTP is enabled.

If you identify a specific error from any the logs, re-run the TSG by selecting "The customer has provided an error".

Engage a TA shall you require help reviewing any of the collected logs.
