<properties
	pageTitle="Site-to-Site VPN connectivity issues"
	description="Site-to-Site VPN connectivity issues"
	service="microsoft.network"
	resource="connections"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32591158"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="2488015e-4081-45d3-bcae-2955d1df176f"
/>

# Site-to-Site VPN connectivity issues

## **Recommended steps**
4 out of 5 customers resolve their Site-to-Site VPN connectivity issues using below steps:<br>
1. Download [VPN device configuration](data-blade:microsoft_azure_network.downloadvpnconfigbladeviewmodel) template<br>
2. [VPN gateway reset](data-blade:microsoft_azure_network.VirtualNetworkGatewayResetBlade) may help if you lost cross-premises VPN connectivity on one or more site-to-site VPN tunnels<br>
3. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade.id.$resourceId)<br>
4. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices<br>
5. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from VM<br>
6. Check if you've configured UDRs or NSGs that may be affecting the connectivity

## **Recommended documents**
* Download [on-premise VPN device configuration script](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection
* Troubleshoot [intermittent disconnections issue](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently) for site-to-site VPN connection
* Troubleshoot site-to-site VPN connection [stopped working and cannot reconnect issue](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-cannot-connect)
* Troubleshoot [on-premises connectivity via VPN gateway](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity#troubleshooting-using-azure-network-watcher) with Network Watcher
* Check list of [validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible
* See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec) to determine tunnel settings for your device
* Configure BGP using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-resource-manager-ps) or [Azure CLI](https://docs.microsoft.com/azure/vpn-gateway/bgp-how-to-cli)
* See [Point-to-Site limitations and FAQ](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S)
