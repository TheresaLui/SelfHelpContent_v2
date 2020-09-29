<properties
    pageTitle="Configure my on-premises VPN device"
    description="Configure my on-premises VPN device"
    service="microsoft.network"
    resource="connections"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="11"
    selfHelpType="resource"
    supportTopicIds="32591152"
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="1337890e-ed19-4e52-9f1b-fc3ec50fb446"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Configure my on-premises VPN device

You can use below help for configuring the on-premises VPN device represented by the local network gateway to establish S2S VPN tunnel with Azure VPN Gateway. You can download the configuration script and use it either as a starting point, or apply the script directly to your on-premises VPN devices via the configuration console.

## **Recommended Steps**

1. Download [VPN device configuration](data-blade:microsoft_azure_network.downloadvpnconfigbladeviewmodel) template <br>
2. Use [VPN Diagnostics](data-blade:microsoft_azure_network.networkwatchervpndiagnosticsblade.id.$resourceId) for troubleshooting on-premise connectivity issues. Review the VPN logs (available in storage account) to find any issues with the VPN tunnel or configuration of devices.

## **Recommended Documents**

* Download [on-premise VPN device configuration script](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript) for site-to-site VPN connection<br>
* Check Azure [Validated VPN Devices List](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-devices) to verify whether your 3rd party device is listed<br>
* Check Azure [3rd party device configuration](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-3rdparty-device-config-overview) for an overview of partner device configurations
