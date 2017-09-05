<properties
	pageTitle="vpn tunnel is down or never connected"
	description="vpn tunnel is down or never connected"
	service="microsoft.network"
	resource="connections"
	authors="radwiv"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32542251"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public"
/>

# vpn tunnel is down or never connected

## **Recommended steps**

1. Check [Resource health](data-blade:microsoft_azure_network.connectionblade) of VPN connections<br>
2. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade)<br>
3. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices<br>
4. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from VM

## **Recommended documents**

Troubleshoot [intermittent disconnections issue for site-to-site VPN](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently)<br>
Troubleshoot [site-to-site VPN connection stopped working and cannot reconnect](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-cannot-connect) issue<br>
Troubleshoot [on-premises connectivity via VPN gateway with Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity#troubleshooting-using-azure-network-watcher)<br>
Check list of [validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible<br>
See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec) to determine tunnel settings for your device
