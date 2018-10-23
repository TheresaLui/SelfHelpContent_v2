<properties
    pageTitle="Site-to-Site VPN connectivity issues"
    description="Site-to-Site VPN connectivity issues"
    service="microsoft.network"
    resource="connections"
    authors="radwiv"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
/>

# Site-to-Site VPN connectivity issues

## **Recommended steps**

4 out of 5 customers resolve their Site-to-Site VPN connectivity issues using below steps:<br>

1. Download [VPN device configuration](data-blade:microsoft_azure_network.downloadvpnconfigbladeviewmodel) template <br>
2. [VPN gateway reset](data-blade:microsoft_azure_network.VirtualNetworkGatewayResetBlade) may help if you lost cross-premises VPN connectivity on one or more site-to-site VPN tunnels<br>
3. Troubleshoot on-premise connectivity issues using [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade.id.$resourceId)<br>
4. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices<br>
5. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from VM

## **Recommended documents**

* Download [on-premise VPN device configuration script](https://docs.azure.cn/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection<br>
* Troubleshoot [intermittent disconnections issue](https://docs.azure.cn/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently) for site-to-site VPN connection<br>
* Troubleshoot site-to-site VPN connection [stopped working and cannot reconnect issue](https://docs.azure.cn/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-cannot-connect)<br>
* Troubleshoot [on-premises connectivity via VPN gateway](https://docs.azure.cn/network-watcher/network-watcher-diagnose-on-premises-connectivity#troubleshooting-using-azure-network-watcher) with Network Watcher<br>
* Check list of [validated VPN devices](https://docs.azure.cn/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure your devices are configured and compatible<br>
* See [IKE parameters](https://docs.azure.cn/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec) to determine tunnel settings for your device
