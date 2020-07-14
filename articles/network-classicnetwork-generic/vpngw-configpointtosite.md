<properties
    pageTitle="Configure a Point-to-Site Gateway for Azure VPN"
    description="Configure a Point-to-Site Gateway for Azure VPN"
    service="microsoft.network"
    resource="virtualnetworkgateways"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="13"
    selfHelpType="generic"
    supportTopicIds="32591148"
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="c439cb2c-ac0f-4ab5-97e4-61df6c138ffb"
   	ownershipId="CloudNet_AzureVPNGateway"
/>

# Configure a Point-to-Site Gateway for Azure VPN

Point-to-Site connections are useful when you want to connect to your virtual network from a remote location, such as when you are telecommuting from home or a conference. Point-to-Site connectivity issues may be due to not having proper VPN profiles on the clients or some other common causes. You can use below help to resolve common Point-to-Site connectivity issues.

## **Recommended Steps**

If you are having problems connecting to your VPN from Windows 7 and Windows 8.1, you may need to enable support for TLS 1.2. Please see [Point-to-Site FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) for additional details.

## **Recommended Documents**

* Step by step guide to [configure a point-to-site gateway](https://support.microsoft.com/help/4032151/configuring-and-validating-vnet-or-vpn-connections)<br>
* Configure a Point-to-Site gateway using [portal](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal) or [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-rm-ps)<br>
* Configure a Point-to-Site VPN connection to a VNet using native Azure certificate authentication using [portal](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal) or [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-rm-ps)<br>
* Create an Azure Active Directory tenant for [Point-to-Site OpenVPN protocol connections](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-tenant)<br>
* Generate self-signed certificates for Point-to-Site using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site), [Makecert](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-makecert), or [Linux](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site-linux)<br>
* [Create an Azure Active Directory tenant](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-tenant) for Point-to-Site OpenVPN protocol connections<br>
* See [Point-to-Site FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) for additional information
