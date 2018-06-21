<properties
    pageTitle="Configure a Point-to-Site connection"
    description="Configure a Point-to-Site connection"
    service="microsoft.network"
    resource="virtualnetworkgateways"
    authors="radwiv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32591148"
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="public"
/>
# Configure a Point-to-Site connection
## **Recommended steps**
Note: Effective July 01' 2018, we'll be supporting only TLS 1.2 from Azure VPN Gateway. TLS 1.0 and 1.1 will not be supported. To maintain TLS support and connectivity for your point-to-site clients using TLS, please install both of the below updates on Windows 7 and Windows 8 (no action required for Windows 10):<br>
[Microsoft EAP implementation that enables use of TLS](https://support.microsoft.com/help/2977292/microsoft-security-advisory-update-for-microsoft-eap-implementation-th)<br>
[Enable TLS 1.1 and TLS 1.2 as default secure protocols in WinHTTP](https://support.microsoft.com/help/3140245/update-to-enable-tls-1-1-and-tls-1-2-as-a-default-secure-protocols-in)

## **Recommended documents**
Step by step guide to [configuring and validating VNet or VPN connections](https://support.microsoft.com/help/4032151/configuring-and-validating-vnet-or-vpn-connections)<br>
Configure a Point-to-Site connection using [portal](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal) or [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-rm-ps)<br>
Generate self-signed certificates for Point-to-Site using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site) or [Makecert](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-makecert)
