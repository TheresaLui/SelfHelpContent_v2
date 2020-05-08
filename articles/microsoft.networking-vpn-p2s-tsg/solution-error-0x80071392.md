<properties
	pageTitle="Solution for VPN Point-to-Site client error 0x80071392"
	description="Solution for VPN Point-to-Site client error 0x80071392"
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
	articleId="f036b9fc-f6ee-4f9e-bc16-627381a39db9"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 0x80071392

The error *"Error 0x80071392: Custom script (to update your routing table) failed"* is due to incorrect routes present on the point-to-site client.

## Recommended Steps

1. On the client, run **route print** from cmd prompt 
2. Remove the persistent route in the client machine routes with the P2S VPN client pool. You can use the Remove-NetRoute [cmdlet](https://docs.microsoft.com/powershell/module/nettcpip/remove-netroute?view=win10-ps)

**_Note_**: If there's such persistent route, Point to Site client will not be able to add a route that already exists
