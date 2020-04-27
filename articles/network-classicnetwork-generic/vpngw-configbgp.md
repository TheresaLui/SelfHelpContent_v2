<properties
    pageTitle="Configure BGP, routing, forced tunneling"
    description="Configure BGP, routing, forced tunneling"
    service="microsoft.network"
    resource="virtualnetworkgateways"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="16"
    selfHelpType="generic"
    supportTopicIds="32591151"
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="7b5af541-1fdd-40f7-88cc-824e4027e949"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Configure BGP, routing, forced tunneling 

BGP enables the Azure VPN Gateways and your on-premises VPN devices, called BGP peers or neighbors, to exchange "routes" that will inform both gateways on the availability and reachability for those prefixes to go through the gateways or routers involved. BGP can also enable transit routing among multiple networks. Forced tunneling lets you redirect or "force" all Internet-bound traffic back to your on-premises location via a Site-to-Site VPN tunnel for inspection and auditing.

## **Recommended Documents**

* Step by step guide to [configuring and validating VNet or VPN connections](https://support.microsoft.com/help/4032151/configuring-and-validating-vnet-or-vpn-connections)
* Configure BGP using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-resource-manager-ps) or [Azure CLI](https://docs.microsoft.com/azure/vpn-gateway/bgp-how-to-cli)
* Configure forced tunneling using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-forced-tunneling-rm)
