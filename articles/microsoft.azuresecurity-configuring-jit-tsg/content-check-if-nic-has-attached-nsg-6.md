<properties
	  pageTitle="Check if NIC has attached NSG"
	  description="Check if NIC has attached NSG"
      service="Microsoft.Compute"
      resource="Microsoft.Compute/virtualMachines,Microsoft.Compute/virtualMachineScaleSets"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="00f0f8a0-6330-4575-bbd2-e866ec534991"
	  ownershipId="Azure_Security_Security_Center"
/>

# Check if NIC has attached NSG

1. Create NSG and attach it the NIC. 
2. It is required even if the NIC has private IP only. 
3. Please refer to [Manage network security groups](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group)
4. JIT operates by creating Allow and Deny rules to the NSG. 
5. All VM's Netwroking must have both in order to be protected by Security Center JIT.
