<properties
	pageTitle="IKE Policy match error (Route Based)"
	description="IKE Policy match error (Route Based)"
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
	articleId="661209f0-a42c-4f13-9c70-3f9d664b589f"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# IKE Policy Match Error (Route Based)

## **Recommended Steps**

 IKE Policy Mismatch error means that one or more of the IPsec parameters offered by Azure gateway is not supported by the on-prem device, or that one or more of the IPsec parameters offered by the on-prem device is not supported by the Azure gateway.

* Identify from IKElogsTable what is the incorrect parameter(s)
* Verify that the customer’s device is in the list of supported VPN devices and that its configuration matches the one linked in the official documentation
* If the customer is using Cisco, Juniper or Ubiquiti devices you can also download the VPN device script from Azure to match the configuration exactly

## **Recommended Documents**

* [VPN Gateways](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices)
* [VPN Gateway Downloads](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript)
