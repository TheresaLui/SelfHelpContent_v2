<properties
	pageTitle="Solution for VPN Point-to-Site client error 1224"
	description="Solution for VPN Point-to-Site client error 1224"
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
	articleId="23d8715e-1331-4320-a488-14c6211a64b6"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 1224

The error *"Error 1224: The operation being requested was not performed because the user has not been authenticated."* is due to incorrect RADIUS settings. Follow the steps below to resolve the issue.

## Recommended Steps

1. An incorrect policy may prevent the connection on the RADIUS server. In this case you need to review Radius logs and identify the incorrect RADIUS setting causing the connection failure
2. If some users can connect and others can’t, there is an issue with the synchronization between the list of users in the customer’s Active Directory and the RADIUS server. We will need to engage Active Directory team for further help on this

## Recommended Documents

* https://docs.microsoft.com/windows-server/networking/technologies/nps/nps-manage-register
