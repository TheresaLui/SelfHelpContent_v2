<properties
	pageTitle="Error X509:parse_pem:error in cert::error:0909006C:PEM routines:get_name:no start line."
	description="Error X509:parse_pem:error in cert::error:0909006C:PEM routines:get_name:no start line."
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
	articleId="6575c088-5fc4-4a79-b487-b98e1d9b41b0"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client Error X509:parse_pem:error in cert::error:0909006C:PEM routines:get_name:no start line.

The error, "Error X509:parse_pem:error in cert::error:0909006C:PEM routines:get_name:no start line.", is an OpenVPN specific error. It is caused by the private key of the certificate on the client side configuration being incorrect.

## Recommended Steps

* Open the **vpnconfig.ovpn** configuration file on the local point to site client
* Browse to the *$PRIVATEKEY* section
* Make sure that the Private Key is correctly added, replacing everything between "key" and "/key".

## Recommended Documents

* [Configure OpenVPN clients for Azure VPN Gateway](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-openvpn-clients)
