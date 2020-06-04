<properties
	pageTitle="Solution for check gateway routes"
	description="Solution for check gateway routes"
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
	articleId="26078b8a-adfe-4ba6-af5c-9d6a1562b8f6"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for check gateway routes

We found that this issue was caused by an undesired 'default site' in the gateway settings. There was another route overriding the correct behavior forcing the traffic in a further tunnel instead of towards destination. 
