<properties
	pageTitle="Check Gateway routes"
	description="Check Gateway routes"
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
	articleId="138e57d5-294b-43d2-97d9-1f60ce0f63d0"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check Gateway routes

If this is the last gateway on the path, but still the gateway is only forwarding traffic on the Inner interface, the gateway is misbehaving. There might be another route overriding the correct behavior forcing the traffic in a further tunnel instead of towards destination. 

Often, this is caused by a forced tunneling rule.

## Recommended Steps

1. Open [Get Gateway](https://jarvis-west.dc.ad.msft.net/?page=actions&acisEndpoint=Public&selectedNodeType=3&extension=Brooklyn&group=Gateway%20Service%20Operations&operationId=getgateway&operationName=Get%20Gateway&inputMode=single&params={"gatewayid":null}&actionEndpoint=Brooklyn%20-%20Prod&genevatraceguid=834f4699-2014-4939-bebe-2740adc95585) from Jarvis Actions and check if a "Default Site" exists for the gateway
2. Remove any Default site that is not desired

## Recommended Documents

1. https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm
