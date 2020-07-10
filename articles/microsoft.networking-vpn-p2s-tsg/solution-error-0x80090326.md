<properties
	pageTitle="Solution for VPN Point-to-Site client error 80090326"
	description="Solution for VPN Point-to-Site client error 80090326"
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
	articleId="5991dc0b-4362-47c9-8759-03ab79f85ff7"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x80090326

The error *"Error 0x80090326: The message received was unexpected or badly formatted"* has multiple potential causes. 

The first is a UDR with default route on the Gateway Subnet. The second is a Master Root Certificate was not uploaded to the Azure gateway or has gotten corrupted or expired. 

## Recommended Steps

1. Remove UDR on the Gateway Subnet, or make sure UDR forwards all traffic properly
2. Check in the 'Point-to-Site configuration' in the 'Virtual Network Gateway' setup in the Azure portal to check on the status of the Master Root Certificate to see if it has been revoked.
