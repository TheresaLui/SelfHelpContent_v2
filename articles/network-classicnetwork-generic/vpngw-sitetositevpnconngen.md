<properties
	pageTitle="Site-to-Site VPN connectivity issues"
	description="Site-to-Site VPN connectivity issues"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder="21"
	selfHelpType="generic"
	supportTopicIds="32591158"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="12fc7bf4-d5a9-4605-a133-d9d6daadae4a"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Site-to-Site VPN connectivity issues

A Site-to-Site VPN gateway connection is used to connect your on-premises network to an Azure virtual network over an IPsec/IKE (IKEv1 or IKEv2) VPN tunnel. See below help to resolve most common issues for Site-to-Site VPN connectivity.

## **Recommended Documents**

* Download [on-premise VPN device configuration script](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection
* Troubleshoot [intermittent disconnections issue](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently) for site-to-site VPN connection
* Troubleshoot site-to-site VPN connection [stopped working and cannot reconnect issue](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-cannot-connect)
* Troubleshoot [on-premises connectivity via VPN gateway](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity#troubleshooting-using-azure-network-watcher) with Network Watcher
* Check list of [validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible
* See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec) to determine tunnel settings for your device
* Configure BGP using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-resource-manager-ps) or [Azure CLI](https://docs.microsoft.com/azure/vpn-gateway/bgp-how-to-cli)
* See [Point-to-Site limitations and FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S)
