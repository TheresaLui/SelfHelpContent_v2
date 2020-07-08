<properties
	pageTitle="Solution for VPN Point-to-Site client error 1460"
	description="Solution for VPN Point-to-Site client error 1460"
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
	articleId="e4efbdf1-913d-4272-a5c6-e3baf516e5c7"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 1460

The error *"Error 1460: VPN Platform did not trigger connection"* is a client-side issue. It happens when the Azure VPN Client app fails to run in background because of Windows OS settings. Azure VPN Client needs to be allowed to run in the background.


## Recommended Steps
1. Go to Start, then select Settings > Privacy > Background apps
2. Under Background Apps, make sure Let apps run in the background is turned On
3. Under Choose which apps can run in the background, turn settings for Azure VPN Client to On
4. Restart the user computer

## Recommended Documents

* [Working with client profiles](https://docs.microsoft.com/azure/virtual-wan/openvpn-azure-ad-client#profile)

