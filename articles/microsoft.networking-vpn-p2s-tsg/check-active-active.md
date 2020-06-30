<properties
	pageTitle="Check active active"
	description="Check active active"
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
	articleId="64caa248-da8c-4025-a243-0c4c33fcc7fe"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check for Active Active Gateway issues

When Active Active is enabled, the Point to site range is divided between the two gateway instances:
- The first half of the range is assigned to Gateway_Tenant_Worker_IN_0
- The second half of the range is assigned to Gateway_Tenant_Worker_IN_1

## Recommended Steps

1. Inspect the VPN client IP addresses assigned to connecting clients and try to determine whether those are coming from IN_0 or IN_1. IF the customer is not using SSTP you can also leverage the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B) to see which gateway instance is servicing the client.
2. If you determine that clients landing on one gateway instance work fine, while clients reaching the other instance don't work, there are two scenarios:
   1. One of the gateway instances may have connectivity issues with the destination (for example it doesn't have a site to site tunnel established). In this case you need to connect all site to site tunnels to on-premises from both instances of the Active Active gateway or migrate the gateway to Active / Passive.
   2. One of the gateway instances may have health issues. You need to troubleshoot the failing gateway instance from a Health perspective.
