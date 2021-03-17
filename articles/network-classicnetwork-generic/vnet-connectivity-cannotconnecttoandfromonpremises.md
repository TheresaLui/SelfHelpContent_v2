<properties
	pageTitle="Diagnose and troubleshoot Azure connectivity issues to and from the on-premises"
	description="Diagnose and troubleshoot Azure connectivity issues to and from the on-premises"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584251"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fee387ea-55c8-4e15-856c-ba26e09faf5b"
	ownershipId="CloudNet_VirtualNetwork"
/>

# Diagnose and fix Azure connectivity issues to and from on-premises

## **Recommended Steps**

1. Use [**IP flow verify**](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to **check if traffic is allowed to or from a virtual machine**<br>
2. [**Resetting your VPN gateway**](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-resetgw-classic#portal) may help if you are consistently losing cross-premises VPN connectivity on one ore more site-to-site VPN tunnels <br>
3. [Troubleshoot on-premises connectivity issues using **VPN Diagnostics**](https://docs.microsoft.com/azure/network-watcher/diagnose-communication-problem-between-networks#diagnose-a-gateway)

## **Recommended Documents**

* [**Verify ExpressRoute connectivity**](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview), whether the issue is in your network, provider network or in the Microsoft data center
* [**Fix connectivity** when a Network Virtual Appliance (NVA) is involved in managing network traffic](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)
* [**Download an on-premises VPN device configuration script**](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript) for your site-to-site VPN connection
* [**Test bandwidth and latency**](https://docs.microsoft.com/azure/virtual-network/virtual-network-bandwidth-testing)
* [**Solve connectivity issues over VNet Peering**](https://support.microsoft.com/help/4486956/troubleshooter-for-virtual-network-peering-issues) <br>
