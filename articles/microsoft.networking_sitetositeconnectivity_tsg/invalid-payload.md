<properties
	pageTitle="Invalid Payload"
	description="Invalid Payload"
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
	articleId="442ec0c5-1f4f-486c-ac41-39ec57bf9668"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Invalid Payload

## **Recommended Steps**

* The IPsec security association failed to get established because the payload sent by the on-prem device is either malformed, or configured in a way not supported by the Azure Gateway.
* Identify from IKElogsTable if there is more detail about the malformed packet
* Verify that the customer’s device is in the list of supported VPN devices and that its configuration matches the one linked in the official documentation
* If the customer is using Cisco, Juniper or Ubiquiti devices you can also download the VPN device script from Azure to match the configuration exactly

## **Recommended Documents**

* [Supported VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices)
* [VPN Device Scripts](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript)
