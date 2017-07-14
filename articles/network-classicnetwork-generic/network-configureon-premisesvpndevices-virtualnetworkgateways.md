<properties
	pageTitle="configure on-premises vpn devices"
	description="configure on-premises vpn devices"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542246"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public"
/>

# configure on-premises vpn devices

## **Recommended steps**
1. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade)
2. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices

## **Recommended documents**
Check list of [validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible<br>
See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-nameipsecaipsecike-parameters) to determine tunnel settings for your device<br>
Check Azure [3rd Party device configuration](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-3rdparty-device-config-overview) to see if your device is available<br>
For Cisco ASA configuration example see [Route Based IKEv2 with CISCO ASA](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-3rdparty-device-config-cisco-asa)<br>
Diagnose [on-premise VPN connectivity issue via VPN gateways](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity)

