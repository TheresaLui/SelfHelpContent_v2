<properties
	pageTitle="Update NSG on Gateway subnet"
	description="Update NSG on Gateway subnet"
	service="microsoft.network"
	resource="vpnGateways"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="50f999b7-9c52-406e-85a5-e306291fd10d"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Update NSG on Gateway subnet

## **Recommended Steps**

* To resolve this issue, add the GatewayManager tag on the subnet
* This will apply the necessary NSG rules to allow traffic
* Alternatively, you may remove the NSG from the Gateway subnet to isolate the issue.
* If the steps above did not resolve the issue, please restart the TSG and select the "VPN doesnt connect" path

## **Recommended Documents**

* [VPN Gateway Settings](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings#gwsub)
* [Virtual Network Security Overview](https://docs.microsoft.com/azure/virtual-network/security-overview#service-tags)
