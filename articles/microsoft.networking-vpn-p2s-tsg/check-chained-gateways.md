<properties
	pageTitle="Check Chained Gateways"
	description="Check Chained Gateways"
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
	articleId="0deb3c01-cbb0-4c0d-bbf0-c5b7eff231fd"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check chained Gateways

If this is the only gateway between the client and the destination (or the last gateway), the traffic must be forwarded on the External (Outer) interface and be visible in the **networktrace.etl** file.

Else if there are more gateways, either Azure VPN gateways or on-premises devices, connected in a chain of site to site connections on the way from point to site client to the destination, it is normal that the traffic is only seen in the **TunnelInnerPacketTrace.etl** file.

The gateway only forwards it on the Inner interface (not on the Outer). <br/>If this is the case, you have proved that the first gateway - the one connected to the Point to Site client is not at fault. However, to identify the cause of the issue you should collect traces on all intermediate gateways during the issue to see which hop might be failing.

## Recommended Steps

1. Check the topology and determine the last gateway
2. Check the last gateway traces to see if the traffic is arriving
