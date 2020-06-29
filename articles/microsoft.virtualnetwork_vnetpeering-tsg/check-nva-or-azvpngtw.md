<properties
	pageTitle="TSG Content Step: Check if customer is using NVA as VPN or Azure VPN gateway"
	description="TSG Content Step: Check if customer is using NVA as VPN or Azure VPN gateway"
	service="microsoft.network"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="dff2e75b-5858-4c95-9120-f3f70f76a0c3"
        ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Check if customer is using NVA as VPN or Azure VPN gateway

It is important to determine what the customer is using as their VNet VPN device. Is it a Network Virtual Appliance (NVA) or is it an Azure VPN Gateway?

## **Recommended Steps**

1. Talk to the custoemr to understand their topology. 
2. In ASC, go to Tools > 'Network Topology' to identify the spoke VNets and Hub VNet.
3. While in the 'Network Topology' tool check the **hub** VNet graphic for a VPN gateway icon (looks like a paddle lock)
4. While in the 'Network Topology' tool check the **spoke** VNet graphic for a VPN gateway icon (looks like a paddle lock)


