<properties
    pageTitle="Configure a Site-to-Site connection"
    description="Configure a Site-to-Site connection"
    service="microsoft.network"
    resource="virtualnetworkgateways"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="12"
    selfHelpType="resource"
    supportTopicIds="32591149"
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="96946134-dccc-4f1b-82fd-925a88e2c37f"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Configure a Site-to-Site connection

A Site-to-Site VPN gateway connection is used to connect your on-premises network to an Azure virtual network over an IPsec/IKE (IKEv1 or IKEv2) VPN tunnel. This type of connection requires a VPN device located on-premises that has an externally facing public IP address assigned to it.

## **Recommended Steps**

1. Use [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade.id.$resourceId) for troubleshoot on-premise connectivity issues
2. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices

## **Recommended Documents**

* Download [on-premise VPN device configuration script](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection
* Step by step guide to [configuring and validating VNet or VPN connections](https://support.microsoft.com/help/4032151/configuring-and-validating-vnet-or-vpn-connections)
* Configure a Site-to-Site connection using [portal](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal), [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-create-site-to-site-rm-powershell) or [Azure CLI](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-cli)
* Configure Site-to-Site and ExpressRoute coexisting connections using [PowerShell](https://docs.microsoft.com/azure/expressroute/expressroute-howto-coexist-resource-manager?toc=%2fazure%2fvpn-gateway%2ftoc.json)
* Configure multiple Site-to-Site connections using [Portal](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-multi-site-to-site-resource-manager-portal) or [PowerShell (classic)](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-multi-site)
* Configure IPSec/IKE policies using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)
* Configure [active-active S2S VPN connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-activeactive-rm-powershell) using VPN Gateways
