<properties
	pageTitle="vpn tunnel is down or never connected"
	description="vpn tunnel is down or never connected"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542251"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public"
/>

# vpn tunnel is down or never connected

## **Recommended steps**
1. Check Resource health of [VPN connection](data-blade:microsoft_azure_network.connectionblade)<br>
2. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade)<br>
3. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices<br>
4. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from VM

## **Recommended documents**
Diagnose [on-premises connectivity via VPN gateway with Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity)<br>
Check list of [validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible<br>
See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-nameipsecaipsecike-parameters) to determine tunnel settings for your device<br>
Gain insights into your Azure Network with [Azure Network Watcher](https://azure.microsoft.com/services/network-watcher/)

