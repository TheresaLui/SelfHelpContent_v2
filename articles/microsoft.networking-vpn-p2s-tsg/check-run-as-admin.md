<properties
	pageTitle="Check Run as Admin"
	description="Check Run as Admin"
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
	articleId="a61bfc85-a4e9-4e8a-8fcf-ac7e97ea100a"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Point to Site Client Requires Admin rights

To use Point to Site VPN, Admin rights are required on the Windows client. The reason for it is that the executable needs admin rights to plumb routes in the local routing table. Without the routes, client won't be able to reach remote networks. This is called out in the documentation: **For Windows clients, you must have administrator rights on the client device in order to initiate the VPN connection from the client device to Azure**.

## Recommended Steps

1. [Ways to check if a user is an administrator in Windows](https://www.isumsoft.com/windows-10/how-to-check-if-i-have-administrator-rights-windows-10.html)

##Recommended Documents

* https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about
