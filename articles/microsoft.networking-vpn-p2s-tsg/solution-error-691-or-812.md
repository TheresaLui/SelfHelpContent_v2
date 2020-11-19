<properties
	pageTitle="Solution for VPN Point-to-Site client error 691"
	description="Solution for VPN Point-to-Site client error 691"
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
	articleId="f4d2cbe1-60d6-42e7-8853-5f6f68950bf4"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 691 and 812.

The errors *"Error: 691: The remote connection was denied because the user name and password combination you provided is not recognized, or the selected authentication protocol you selected is not permitted on the remote access server."*  and *"Error 812 the connection was prevented because of a policy configured on your RAS/VPN server"* are due to either incorrect TLS settings or incorrect RADIUS settings.

## How to solve the issue

1. The client may be using a TLS version lower than 1.2. Configure the client to use TLS 1.2 as per  https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#tls1

2. If using RADIUS
* Some incorrect policy may prevent the connection on the RADIUS server itself, in which case you need to advice customer to review Radius logs and identify the incorrect RADIUS setting causing the connection failure

* If some users can connect and others can’t, there is an issue with the synchronization between the list of users in the customer’s Active Directory and the RADIUS server. Please engage Active Directory team for further help on this

* Another cause could be that the RADIUS server is unreachable from the VPN gateway: you can determine that by collecting simultaneous packet captures on the Gateway and on the RADIUS server



