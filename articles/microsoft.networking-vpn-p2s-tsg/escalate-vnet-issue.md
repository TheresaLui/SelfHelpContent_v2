<properties
	pageTitle="Escalate Vnet issue"
	description="Escalate Vnet issue"
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
	articleId="d900ca67-fe7d-449f-b2dc-cb0ac00c0683"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Escalate - Vnet issue

If the last gateway on the path between client and destination is sending packets correctly on its external interface, but they don't make it to the destination, it means that the packets are lost on the path between gateway and destination.

- This is no longer a VPN issue - the gateway is not at fault. The case is to be categorized as a Vnet issue. 

- Please continue troubleshooting the case as if it was a Vnet issue.

- Engage a TA if you need further help with troubleshooting Vnet issues.
