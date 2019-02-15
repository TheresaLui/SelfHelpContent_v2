<properties
	pageTitle="Point to site VPN connectivity issues"
	description="Point to site VPN connectivity issues"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32591156"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public"
	articleId="741dca88-bfab-43ba-8d4b-c8f04a65f4a3"
/>

# Point to site VPN connectivity issues

## **Recommended steps**

1. Please note that Azure VPN Gateway no longer uses self-signed certificates for P2S connections. You may need to download the VPN profile and redeploy to clients. See [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-point-to-site-gateway-public-ca) for aditional details.<br>  
2. If you are having problems connecting to your VPN from Windows 7 and Windows 8.1, you may need to enable support for TLS 1.2. Please see [Point-to-Site FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) for additional details. 

## **Recommended documents**
* Troubleshoot [point-to-site connection issues](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-vpn-point-to-site-connection-problems)<br>
* Configure a [point-to-site VPN Gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal)<br>
* Generate self-signed certificates for Point-to-Site using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site), [Makecert](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-makecert) or [Linux](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-linux)<br>
* Check [point-to-site connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) details
