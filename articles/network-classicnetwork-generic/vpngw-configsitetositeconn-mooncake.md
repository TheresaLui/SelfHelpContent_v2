<properties
    pageTitle="Configure a Site-to-Site connection"
    description="Configure a Site-to-Site connection"
    service="microsoft.network"
    resource="connections"
    authors="radwiv"
    displayOrder="2"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
/>

# Configure a Site-to-Site connection

## **Recommended steps**

1. Download [VPN device configuration](data-blade:microsoft_azure_network.downloadvpnconfigbladeviewmodel) template
2. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade.id.$resourceId)
3. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices

## **Recommended documents**

* Download [on-premise VPN device configuration script](https://docs.azure.cn/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection
* Step by step guide to [configuring and validating VNet or VPN connections](https://support.microsoft.com/help/4032151/configuring-and-validating-vnet-or-vpn-connections)
* Configure a Site-to-Site connection using [portal](https://docs.azure.cn/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal), [PowerShell](https://docs.azure.cn/vpn-gateway/vpn-gateway-create-site-to-site-rm-powershell) or [Azure CLI](https://docs.azure.cn/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-cli)
* Configure Site-to-Site and ExpressRoute coexisting connections using [PowerShell](https://docs.azure.cn/zh-cn/expressroute/expressroute-howto-coexist-resource-manager?toc=%2fazure%2fvpn-gateway%2ftoc.json)
* Configure multiple Site-to-Site connections using [Portal](https://docs.azure.cn/vpn-gateway/vpn-gateway-howto-multi-site-to-site-resource-manager-portal) or [PowerShell (classic)](https://docs.azure.cn/vpn-gateway/vpn-gateway-multi-site)
* Configure IPSec/IKE policies using [PowerShell](https://docs.azure.cn/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell)
* Configure [active-active S2S VPN connections](https://docs.azure.cn/vpn-gateway/vpn-gateway-activeactive-rm-powershell) using VPN Gateways