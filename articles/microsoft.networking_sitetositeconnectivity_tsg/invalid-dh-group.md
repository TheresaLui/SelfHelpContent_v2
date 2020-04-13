<properties
	pageTitle="Invalid DH Group"
	description="Invalid DH Group"
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
	articleId="e434a646-fae3-4a57-b59d-848142a12b1f"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Invalid DH Group

## **Recommended Steps**

* With default settings, Azure VPN gateways only support DHgroup2.
* With custom IPsec policies, we can support multiple (see link below)
* Either way, the DH group used by the customer’s device is not the one configured on the IPsec policy (default or custom).  
* Tell customer to check the their device

## **Recommended Documents**

* [Configure IPsec/IKE policy for S2S VPN or VNet-to-VNet connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)
