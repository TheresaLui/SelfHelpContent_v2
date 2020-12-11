
<properties
pageTitle="Diagnose and resolve site-to-Site VPN connectivity issues" 
description="Diagnose and resolve site-to-Site VPN connectivity issues" 
ms.author="mariliu"
displayOrder=""
articleId="3db8d5b4-ba43-49c2-8f0b-93cb9c9d752e" 
selfHelpType="Apollo"
supportTopicIds="8512ac34-796e-7c4b-0d37-6c5de3624e50"
productPesIds="16094"
cloudEnvironments="public"
ownershipId="CloudNet_AzureVPNGateway"
/>

# Diagnose and resolve Site-to-Site VPN connectivity issues <Internal>
## Troubleshoot Site-to-Site VPN connectivity issues
:::Section VPN connectivity:::

A Site-to-Site VPN gateway connection connects your on-premises network to an Azure virtual network over an IPsec/IKE (IKEv1 or IKEv2) VPN tunnel. 

Insights from the the following diagnostics can help you troubleshoot most Site-to-Site VPN connectivity issues. If diagnostics don’t detect an issue, the following recommended steps and documents can help you troubleshoot further.

### VPN Gateway diagnostics

<Insight>
<symptomId>BrooklynLogEventInsights</symptomId>
<executionText>We are running diagnostic on your VPN Gateway to detect common issues.</executionText>
<timeoutText>We stopped the check because it was taking too long.</timeoutText> 
<noResultText>Diagnostics did not detect any issue with your VPN Gateway. Please review the following additional solutions.</noResultText> 
<additionalInputsReq>false</additionalInputsReq>
</Insight>

### GatewaySubnet diagnostics 

<Insight>
<symptomId>ServiceEndpointPolicy-on-GatewaySubnet</symptomId>
<executionText>We are running diagnostics on your GatewaySubnet to detect anomalies.</executionText>
<timeoutText>We stopped the check because it was taking too long.</timeoutText> 
<noResultText>Diagnostics did not detect any issues on your GatewaySubnet. Please review the following additional solutions.</noResultText>
<additionalInputsReq>false</additionalInputsReq>
</Insight>

## Recommended steps

1. [VPN Gateway reset](data-blade:microsoft_azure_network.VirtualNetworkGatewayResetBlade) can help if you lost cross-premises VPN connectivity on one or more site-to-site VPN tunnels<br>
2. Troubleshoot on-premises connectivity issues by using [VPN diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade.id.$resourceId)<br>
3. Review the VPN logs (available in the storage account) to find any issues with the VPN tunnel or configuration of devices<br>
4. Use [packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from the VM<br>
5. Check if you've configured UDRs or NSGs that may be affecting the connectivity

## More resources

* Download the [on-premises VPN device configuration script](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection
* Troubleshoot [intermittent disconnection issues](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-disconnected-intermittently) for site-to-site VPN connections
* Troubleshoot the [stopped working and cannot reconnect issue](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-site-to-site-cannot-connect) for site-to-site VPN connections
* Troubleshoot [on-premises connectivity through the VPN Gateway](https://docs.microsoft.com/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity#troubleshooting-using-azure-network-watcher) with Network Watcher
* Check the [list of validated VPN devices](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#a-namedevicetableavalidated-vpn-devices-and-device-configuration-guides) to ensure that your devices are configured and compatible
* See [IKE parameters](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices#ipsec) to determine tunnel settings for your device
* Configure BGP by using [PowerShell](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-resource-manager-ps) or [Azure CLI](https://docs.microsoft.com/azure/vpn-gateway/bgp-how-to-cli)
* See [Point-to-Site limitations and FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S)
