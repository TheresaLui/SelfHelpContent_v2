<properties
	pageTitle="Guidelines (other OS)"
	description="Guidelines (other OS)"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="891bad3d-c489-4516-8623-de049378bb14"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check guidelines for Other OS

When troubleshooting Point to Site issue with non-Windows clients, the customer needs to understand that our support is limited.
We can only debug the Gateway side, and if we determine that the issue is on the client side, we might need to ask the customer to troubleshoot that on their own.

## Recommended Steps

**Have customer follow the documentation below for proper installation of their clients**

1. [Linux StrongSwan GUI - IKEv2](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-vpn-client-configuration-azure-cert#linuxgui)
1. [Linux StrongSwan CLI - IKEv2](https://docs.microsoft.com/azure/vpn-gateway/point-to-site-vpn-client-configuration-azure-cert#linuxinstallcli)
1. [IOS OpenVPN](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-openvpn-clients#iOS) requires IOS version 11.0 and OpenVPN version 2.4
1. [Linux OpenVPN](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-openvpn-clients#linux)
1. Windows ARM64 devices like Surface Pro X now support the Azure VPN Client which can be installed from the Microsoft Store (no public Doc available yet).
1. Customer must use Windows using Azure VPN client with OpenVPN to leverage Azure AD authentication
1. [Other OS are not supported](https://docs.microsoft.com/azure/vpn-gateway/openvpn-azure-ad-client).

Once customer has correctly installed the client as per the guidelines, we can troubleshoot on the gateway side if the issue still exists.

**Collecting traces on the Azure VPN Gateway**

1. Identify the VPN gateway in ASC.
1. From the **Diagnostics** tab, select **Brooklyn Diagnostics** and **Create Diagnostics report**
1. Choose the duration in minutes and click **Run**
1. *Reproduce the connectivity issue*
1. After the diagnostic operation is completed, you can download the zip file containing the traces
1. The most relevant file for point to site connection is the **networktrace.etl** (packet capture on the gateway side)
1. Other than a live trace, remember than text-based logging is available on Jarvis at the [P2SlogsTable](https://jarvis-west.dc.ad.msft.net/81FCCD6B) (valid for both OpenVpn and IKEv2) and [IkeLogsTable](https://jarvis-west.dc.ad.msft.net/A5B239BD). Data is normally filled in Jarvis 5-10 minutes after the repro.

If you identify a specific error from any the logs, re-run the TSG by selecting "The customer has provided an error".

Engage a TA shall you require help reviewing any of the collected logs.
