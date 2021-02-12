<properties
	pageTitle="IKE Policy match error"
	description="IKE Policy match error"
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
	articleId="8c954922-249b-48a3-aa02-98c545dd26d3"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# IKE Policy Match Error

## **Recommended Steps**

 IKE Policy Mismatch error means that one or more of the IPsec parameters offered by Azure gateway is not supported by the on-prem device, or that one or more of the IPsec parameters offered by the on-prem device is not supported by the Azure gateway.

* Identify from WFPdiag.txt what is the incorrect parameter(s)
* Verify that the virtual network address range and on-prem network (local gateway) subnets match exactly on both the Azure Gateway configuration and the on-prem device configuration
* Verify that the customer’s device is in the list of supported VPN devices and that its configuration matches the one linked in the official documentation

## **Recommended Documents**

* [VPN Gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices)
