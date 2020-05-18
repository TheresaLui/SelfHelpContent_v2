<properties
	pageTitle="Solution-forced-tunneling-notsupported"
	description="Solution-forced-tunneling-notsupported"
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
	articleId="9522f2fe-cb4b-4c8a-8a64-8530f160c236"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Point to Site Force Tunneling is NOT supported.

- Customers would like all traffic sent by the Point to Site client to be forwarded to the Azure VPN gateway, and be redirected to the final destination by the Azure VPN Gateway itself using an Azure Public IP address as source.
- Normally the intent is to circumvent Firewall restrictions on the client's source IP address - thus the desire to use an AzureIP.
- Many customers have been asking for this feature, but it is NOT supported by the Azure Point to Site implementation.

## Recommended Steps

Only solution is NOT using Azure native VPN Gateway with Point to Site functionality but a third party VPN gateway on Azure.
1. Configure a third party NVA on Azure to act both as VPN gateway and router
2. Configure routes on the point to site client to force tunnel all traffic to the NVA
3. Configure the third party NVA to forward to the internet the traffic received on their VPN interface


## Recommended Documents

- https://azure.microsoft.com/en-us/solutions/network-appliances/
