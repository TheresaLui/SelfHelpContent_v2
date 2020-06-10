<properties
	pageTitle="Basic SKU doesn't support IKEv2"
	description="Basic SKU doesn't support IKEv2"
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
	articleId="2eb3f89b-0950-43c9-9e85-cb3920fb7647"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check gateway SKU and protocol

## Recommended Steps

1.    Go to ASC > Resource Explorer and select the VPN gateway 
2.    Check the **GatewaySKU** property for 'Basic' or 'Default'
3.    Check the **VPN Tunneling Protocols** property to identify the protocol in use

## More Information

Basic SKU doesn't support IKEv2 nor OpenVPN.

* A classic gateway or Basic SKU does not support IKEv2 nor OpenVPN.
* For this reason the  classic gateway or Basic SKU only supports SSTP (and Windows clients).

## Recommended documents

* https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways#gwsku
