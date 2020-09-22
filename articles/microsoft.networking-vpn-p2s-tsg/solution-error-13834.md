<properties
	pageTitle="Solution for VPN Point-to-Site client error 13834"
	description="Solution for VPN Point-to-Site client error 13834"
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
	articleId="fcfa0495-a38e-4fe3-830a-2b7892a54a82"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client error 13834

The error *"Connection was prevented because of error 13834 = Error processing ID payload"* is an error raised by the IPsec stack on Windows OS client when parsing the Traffic Selector payload. The Windows OS client supports a maximum of 25 Traffic Selectors. Any amount of TS higher than 25 will cause the failure with error 13834. For the point to site connections, a Traffic Selector is added for each subnet in each local network connected to the VPN gateway via site to site. 

## Recommended Steps

1. Modify the on-premises IP address prefixes by combining multiple on-premises subnets using CIDR until the total is less than 25

## Recommended Documents

* [Modify local network gateway settings using the Azure portal](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-modify-local-network-gateway-portal)

