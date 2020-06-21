<properties
	pageTitle="Collect Packet Captures (Disconnected)"
	description="Collect Packet Captures (Disconnected)"
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
	articleId="74eae176-f196-4dcd-9ec7-693f0663b1ff"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Collect Packet Captures in 'Can't connect or Disconnected' scenario

If the point to site VPN is disconnected, and it seems like not even the gateway is healthy (not responding to health probe on port 8081) there might be an issue on the gateway itself or in our network infrastructure.

Next troubleshoting step is to collect Packet captures **simultaneously** on the:

- Your Microsoft provided laptop/workstation
- Azure VPN Gateway

Notice how it doesn't matter involving the customer for data collection here. Since the gateway appears unealthy even for out tests, we can troubleshoot on our own.

During data analysis, filter traffic on the network traces according to your scenario based on the IP and ports required for your scenario. Do NOT apply traffic filters upon data collection as they may prevent you from troubleshooting properly.

## Recommended Steps

**Collecting traces on Point to site client**

1. Start a Network capture by running **netsh trace start report=disabled capture=yes tracefile=C:\VPNclient_trace.etl** from an elevated command prompt
1. *Reproduce the connectivity issue by trying to reach port 8081 from the client*
1. Stop the network capture by running **netsh trace stop** from an elevated command prompt

**Collecting traces on the Azure VPN Gateway**

1. Identify the VPN gateway in ASC.
1. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
1. Choose the duration in minutes and click **Run**
1. *Reproduce the connectivity issue by trying to reach port 8081 from the client*
1. After the diagnostic operation is completed, you can download the zip file containing the traces
1. The most relevant files for this test is the **networktrace.etl** (packet capture on the gateway side)

**Note**: if the gateway is not healthy, chances are that you won't be even able to connect to it to collect diagnostics.

In either case, please engage a TA for potential escalation if you reach this point in the TSG.
