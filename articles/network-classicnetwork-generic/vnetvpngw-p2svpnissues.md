<properties
	pageTitle="p2s vpn issues"
	description="p2s vpn issues"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584878"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fbbd16a1-4abf-48c3-a9ca-7834280dc5ae"
	ownershipId="CloudNet_VirtualNetwork"
/>

# p2s vpn issues

## **Recommended steps**
Note: Effective July 01' 2018, we'll be supporting only TLS 1.2 from Azure VPN Gateway. TLS 1.0 and 1.1 will not be supported. To maintain TLS support and connectivity for your point-to-site clients using TLS, please install both of the below updates on Windows 7 and Windows 8 (no action required for Windows 10):<br>
[Microsoft EAP implementation that enables use of TLS](https://support.microsoft.com/help/2977292/microsoft-security-advisory-update-for-microsoft-eap-implementation-th)<br>
[Enable TLS 1.1 and TLS 1.2 as default secure protocols in WinHTTP](https://support.microsoft.com/help/3140245/update-to-enable-tls-1-1-and-tls-1-2-as-a-default-secure-protocols-in)

## **Recommended documents**
Troubleshoot [point-to-site connection issues](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-vpn-point-to-site-connection-problems)<br>
Check [point-to-site connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) details<br>
Configure a [point-to-site VPN connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal)<br>
Generate and export [certificates for point-to-site connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site) for Windows 10
