<properties
    pageTitle="Configure a Point-to-Site Gateway"
    description="Configure a Point-to-Site Gateway"
    service="microsoft.network"
    resource="virtualnetworkgateways"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="13"
    selfHelpType="generic"
    supportTopicIds="32591148"
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
    articleId="c439cb2c-ac0f-4ab5-97e4-61df6c138ffb"
/>
# Configure a Point-to-Site Gateway

Point-to-Site VPN connections are useful when you want to connect to your virtual network from a remote location, such as when you are telecommuting from home or a conference. Point-to-Site connections do not require a VPN device or a public-facing IP address. Point-to-Site connections are created over either SSTP (Secure Socket Tunneling Protocol), or IKEv2.

## **Recommended steps**
If you are having problems connecting to your VPN from Windows 7 and Windows 8.1, you may need to enable support for TLS 1.2. Please see [Point-to-Site FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) for additional details.

## **Recommended documents**
* Step by step guide to [configure a point-to-site gateway](https://support.microsoft.com/help/4032151/configuring-and-validating-vnet-or-vpn-connections)
* Configure a Point-to-Site gateway using [portal](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal) or [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-rm-ps)
* Generate self-signed certificates for Point-to-Site using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site), [Makecert](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-makecert) or [Linux](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-linux)
