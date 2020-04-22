<properties
	pageTitle="TSG Content Step: Check on prem device config for remote range"
	description="TSG Content Step: Check on prem device config for remote range"
	service="microsoft.network"
	ownershipid="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ad9a46c2-8bcd-4b80-be12-4e27fade34c3"
/>

# Check on-prem device config for spoke VNet IP range

If the customer is not using a BGP enabled VPN gateway the on-premises VPN device will not automatically 'learn' the routes added through VPN peering. They must be added manually. This step is often overlooked by customers so it is something we should check. The on-Premises devices need the remote Vnet address space added.

## **Recommended Steps**

1. Have the customer check the on-premises device configuration. It will vary depending on the device make/model. We should ask the customer to check the on-premises device configuration to validate it has the peered VNet ranges and have them send the configuration to us for validation.



