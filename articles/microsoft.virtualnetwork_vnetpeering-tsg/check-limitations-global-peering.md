<properties
	pageTitle="TSG Content Step: Check for Global Peering Limitations and Constraints"
	description="TSG Content Step: Check for Global Peering Limitations and Constraints"
	service="microsoft.network"
	ownershipId="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d81fb70f-cb3b-480c-a6a4-d68474261748"
/>

# Check for Global Peering Limitations and Constraints

We want to check if the customer is leveraging ***Global VNet Peering*** (peering between VNets that are in different regions). The reason is that there are limitations to this type of peering and we want to make sure we catch them early and inform the customer.

## **Recommended Steps**

1. Get the names of the VNets that customer has peered.
2. In ASC Resource Explorer, check the 'Location' property of each VNet
3. Are the VNet locations different? 

	1. If not, you can move to the next step
	2. If yes, review the items below and the 'Limitations and Constraints' link below and ask the customer if any of these are involved in the connectivity
	
4. Check the known limitations and constraints as one cannot connect to the following resources over Global VNet Peering

	1. VMs behind Basic ILB SKU
	2. Redis Cache (uses Basic ILB SKU)
	3. Application Gateway (uses Basic ILB SKU)
	4. Scale Sets (uses Basic ILB SKU)
	5. Service Fabric clusters (uses Basic ILB SKU)
	6. SQL Always-on (uses Basic ILB SKU)
	7. App Service Environments (ASE) (uses Basic ILB SKU)
	8. API Management (uses Basic ILB SKU)
	9. Azure Active Directory Domain Service (ADDS) (uses Basic ILB SKU)
	10. VNet Integration (SWIFT) resources cannot communicate with resources in a globally peered VNet

## **Recommended Documents**

1. [Global Peering Requirements and Constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview#requirements-and-constraints)




