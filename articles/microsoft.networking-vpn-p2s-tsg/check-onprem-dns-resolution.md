<properties
	pageTitle="Check Onprem DNS Resolution"
	description="Check Onprem DNS Resolution"
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
	articleId="92594f18-a574-4e7f-839b-1ce2d3ac164c"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# How to check customer DNS configuration

## Recommended Steps

1. Normally point to site clients use the DNS servers specified on the Point to Site interface (which are the DNS servers defined for the Azure virtual network)
2. These DNS servers might not be able to perform DNS resolution for on-prem resources
3. If using Windows, the customer ip configuration can be determined from the output of **ipconfig /all**
