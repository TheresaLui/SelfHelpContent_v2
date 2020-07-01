<properties
	pageTitle="SSTP Client Connection Limit"
	description="SSTP Client Connection Limit"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="449eb3b9-3175-4f5d-a164-4c0abe431e37"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check for SSTP Client Connection Limit

SSTP in Azure VPN gateway is implemented via Routing and Remote Access server role. For this reason, we are limited to max 128 point to site clients for every SKU. You can check if the customer is exceeding the number of clients by checking the guide below

## **Recommended Documents**

* https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/134255/Point-to-Site-VPN-Issues?anchor=too-many-p2s-clients-connected-at-once
