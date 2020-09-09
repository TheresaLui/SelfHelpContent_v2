<properties
	pageTitle="Check Overlaps"
	description="Check Overlaps"
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
	articleId="d560065c-348d-439d-8f6e-0cd541779227"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check for IP Address Overlaps

1. Identify Point to site Range
   1. Go to ASC > Resource Explorer and select the VPN gateway
   2. Check the **VPN Client Address Pool** property. This is the point to site range
2. Identify Virtual Network Address Space
   1. Go to ASC > Resource Explorer and select the VPN gateway
   2. Find the **Virtual Network Name** where the gateway is and click on the Hyperlink to open the Vnet
   3. Identify the Virtual Network Address space
3. Identify On-premises ranges - the customer must provide this information, as it's not saved in Azure.
