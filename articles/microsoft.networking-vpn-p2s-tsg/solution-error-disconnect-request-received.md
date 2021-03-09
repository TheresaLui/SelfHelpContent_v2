<properties
	pageTitle="VPN Point-to-Site client error Disconnect request received - Remote initiated"
	description="VPN Point-to-Site client error Disconnect request received - Remote initiated"
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
	articleId="809ad8af-be47-4be7-ac67-23bce254b303"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# VPN Point-to-Site client error **Disconnect request received <= Remote initiated**

The general elements of this error are:

1. The customer is using OpenVPN with Azure VPN Client
2. The point-to-site client connects with no issues, but after 20 to 60 seconds, it disconnects unexpectedly
3. The point-to-site logs on the Gateway say, "Disconnect request received <= Remote initiated," confirming that the issue is on client side
4. But client logs say, "The operation was cancelled by the user," although the user didn't cancel the operation

**This is a Windows OS issue**. There are multiple reasons why this might happen, so there is not a single solution. Generally, you can fix the issue by changing the client (proving the issue is on the client side) or by running Windows Updates.

Either way, it's not an Azure networking issue but a Windows issue.

## Recommended Steps

1. Install latest Windows hotfixes on the client by running Windows Update
2. If issue the persists, work with the Windows Networking team through a Service Desk collaboration
