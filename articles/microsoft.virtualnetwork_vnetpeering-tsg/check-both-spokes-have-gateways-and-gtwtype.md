<properties
	pageTitle="TSG Content Step: Check if both spoke and hub vnets have VPN gateway"
	description="TSG Content Step: Check if both spoke and hub vnets have VPN gateway"
	service="microsoft.network"
	ownershipid="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="bcde54fa-7138-4001-b54a-dccb5fe06042"
/>

# Check if both spoke and hub vnets have VPN gateways

When a customer is trying to reach a spoke VNet from on-premises only the hub VNet can have a VPN gateway. Having gateways in both the spoke VNet and the hub VNet will not work.

## **Recommended Steps**

1. Understand the customers topology. In ASC, go to Tools > 'Network Topology' to identify the spoke VNets and Hub VNet.
2. While in the 'Network Topology' tool check the **hub** VNet graphic for a VPN gateway icon (looks like a paddle lock)
3. While in the 'Network Topology' tool check the **spoke** VNet graphic for a VPN gateway icon (looks like a paddle lock)


