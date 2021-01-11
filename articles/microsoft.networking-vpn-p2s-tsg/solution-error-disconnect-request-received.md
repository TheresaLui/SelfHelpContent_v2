<properties
	pageTitle="VPN Point-to-Site client error Disconnect request received <= Remote initiated"
	description="VPN Point-to-Site client error Disconnect request received <= Remote initiated"
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

General symptoms for this error are:

1. Customer is using OpenVPN with Azure VPN Client
2. Point to site client connects just fine
3. After some 20 to 60 seconds, it disconnects unexpectedly
4. Point to site logs on the Gateway say "Disconnect request received <= Remote initiated" confirming the issue is on client side
5. But client logs say "The operation was cancelled by the user" while it wasn't the user cancelling the operation



**This is a Windows OS issue**. There are multiple reasons why this might happen, hence there is not an unique solution. Generally the issue is fixed by changing client (proving the issue is on client side) or running Windows Updates.

Either way it's not an Azure Networking issue but a Windows issue.

## Recommended Steps

1. Install latest Windows hotfixes on the client by running Windows Update
2. If issue isn't solved, engage Windows Networking team via Service Desk collaboration
