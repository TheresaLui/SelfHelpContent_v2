<properties
	pageTitle="Diagnose and resolve site-to-Site VPN connectivity issues"
	description="Diagnose and resolve site-to-Site VPN connectivity issues"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder="21"
	selfHelpType="resource"
	supportTopicIds="32591158"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cc230e94-e48b-46d4-9f87-d618a6fe01ff"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Diagnose and resolve site-to-Site VPN connectivity issues

A Site-to-Site VPN gateway connection is used to connect your on-premises network to an Azure virtual network over an IPsec/IKE (IKEv1 or IKEv2) VPN tunnel. 4 out of 5 customers resolve their Site-to-Site VPN connectivity issues using below steps.<br>

## **Recommended Steps**

1. [VPN gateway reset](data-blade:microsoft_azure_network.VirtualNetworkGatewayResetBlade) may help if you lost cross-premises VPN connectivity on one or more site-to-site VPN tunnels<br>
2. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade.id.$resourceId)<br>
3. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices<br>
4. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from VM<br>
5. Check if you've configured UDRs or NSGs that may be affecting the connectivity

## **Recommended Documents**

* Download [on-premise VPN device configuration script](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection
* Troubleshoot [intermittent disconnections issue](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently) for site-to-site VPN connection
* Troubleshoot site-to-site VPN connection [stopped working and cannot reconnect issue](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-cannot-connect)
* Troubleshoot [on-premises connectivity via VPN gateway](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity#troubleshooting-using-azure-network-watcher) with Network Watcher
* Check list of [validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible
* See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec) to determine tunnel settings for your device
* Configure BGP using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-resource-manager-ps) or [Azure CLI](https://docs.microsoft.com/azure/vpn-gateway/bgp-how-to-cli)
* See [Point-to-Site limitations and FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S)
