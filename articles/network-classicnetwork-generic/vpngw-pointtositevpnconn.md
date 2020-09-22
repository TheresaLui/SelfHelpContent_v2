<properties
	pageTitle="Point to site VPN connectivity issues"
	description="Point to site VPN connectivity issues"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder="22"
	selfHelpType="generic"
	supportTopicIds="32591156"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="741dca88-bfab-43ba-8d4b-c8f04a65f4a3"
	OwnershipId="CloudNet_AzureVPNGateway"
/>

# Point to site VPN connectivity issues

Point-to-Site connections are useful when you want to connect to your virtual network from a remote location, such as when you are telecommuting from home or a conference. Point-to-Site connectivity issues may be due to not having proper VPN profiles on the clients or some other common causes. You can use below help to resolve common Point-to-Site connectivity issues.

## **Recommended Steps**

If you are having problems connecting to your VPN from Windows 7 and Windows 8.1, you may need to enable support for TLS 1.2. Please see [Point-to-Site FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) for additional details. 

## **Recommended Documents**

* Troubleshoot [point-to-site connectivity issues](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-vpn-point-to-site-connection-problems)<br>
* Troubleshoot point-to-site connectivity issues for [Mac OS X using VPN client](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-point-to-site-osx-ikev2)<br>
* Troubleshoot [Azure VPN client connection issues](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-client#diagnose)<br>
* Configure a [point-to-site VPN Gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal)<br>
* Generate self-signed certificates for Point-to-Site using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site), [Makecert](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-makecert) or [Linux](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-linux)<br>
* Check [point-to-site connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) details<br>
* [Create an Azure Active Directory tenant](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-tenant) for Point-to-Site OpenVPN protocol connections
