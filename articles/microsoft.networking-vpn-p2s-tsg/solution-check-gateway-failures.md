<properties
	pageTitle="Solution for check gateway failures"
	description="Solution for check gateway failures"
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
	articleId="d9028228-8997-4a4e-b9fe-f3d35dd30191"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for check gateway failures

Through our troubleshooting and review of the Azure VPN gateway logs we determined that issue was caused by maintenance on the gateways. In such circumstances, all point to site clients are disconnected by design.

##Recommended Steps

1. Have the point-to-site users reconnect their VPN connection.


##Recommended Documents

* [Point-to-site clients disconnected during gateway failover](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-highlyavailable)

