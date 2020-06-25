<properties
	pageTitle="Solution for VPN Point-to-Site client error 720"
	description="Solution for VPN Point-to-Site client error 720"
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
	articleId="6c818cff-1f82-4f3f-9b87-54651bee7a36"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 720

The error *"Error 720: No PPP control protocols configured"* is specific to the Windows OS networking stack. This is a client-side issue as the TCP/IP stack may be corrupted and the client isn't able to find a suitable PPP protocol to use.

## Recommended steps

1. Open elevated command prompt on the client
2. Run **netsh int ip reset**
3. Reboot the client
  