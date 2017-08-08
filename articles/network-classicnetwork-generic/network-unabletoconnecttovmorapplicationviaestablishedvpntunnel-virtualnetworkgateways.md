<properties
	pageTitle="unable to connect to vm or application via established vpn tunnel"
	description="unable to connect to vm or application via established vpn tunnel"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542249"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public"
/>

# unable to connect to vm or application via established vpn tunnel

## **Recommended steps**
1. Check Resource health of VPN connections
2. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade)
3. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices
4. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from VM
5. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade) to check if traffic is allowed to or from a virtual machine

## **Recommended documents**
Check list of [validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible<br>
See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-nameipsecaipsecike-parameters) to determine tunnel settings for your device<br>
Diagnose [on-premises connectivity via VPN gateway with Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity)<br>
Check traffic with [IP flow verify over VPN connection](https://docs.microsoft.com/azure/network-watcher/network-watcher-check-ip-flow-verify-portal)<br>
Gain insights into your Azure Network with [Azure Network Watcher](https://azure.microsoft.com/services/network-watcher/)

