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

The following errors are caused by incorrect TLS settings or incorrect RADIUS settings:
	* "Error: 691: The remote connection was denied because the user name and password combination you provided is not recognized, or the selected authentication protocol you selected is not permitted on the remote access server."
	* "Error 812 the connection was prevented because of a policy configured on your RAS/VPN server"

## How to solve the issue

1. The client may be using a TLS version earlier than 1.2. [Configure the client to use TLS 1.2](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-about#tls1).

2. If using RADIUS:
   * Incorrect policies may prevent the connection on the RADIUS server itself. Advise the customer to review their RADIUS logs for incorrect RADIUS settings that may be causing the connection failure.

   * If some users can connect and others can’t, there is an issue with the synchronization between the list of users in the customer’s Active Directory and the RADIUS server. Contact the Active Directory team for further help on this.

   * Another cause could be that the RADIUS server is unreachable from the VPN gateway: you can determine that by collecting simultaneous packet captures on the Gateway and on the RADIUS server

   * Additionally, this issue can be triggered if the customer may has more than one VPN gateway connected to each other; both configured with the same (or overlapping) point-to-site address range.


