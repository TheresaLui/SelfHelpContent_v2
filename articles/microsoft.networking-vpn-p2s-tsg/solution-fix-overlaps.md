<properties
	pageTitle="Solution for overlapping ranges between Azure and Onprem"
	description="Solution for overlapping ranges between Azure and Onprem"
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
	articleId="41e008c2-b524-4d10-8432-5fbdbd0eb709"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

The address space cannot overlap between Azure and customer premises

## Recommended Steps

1. Have the customer verify that the point to site client range is NOT overlapping with any of the customer’s on-premises networks (There is no means to verify this on the Azure side)
2. The customer needs to choose a valid non-overlapping Point to Site IP range according to their environment

