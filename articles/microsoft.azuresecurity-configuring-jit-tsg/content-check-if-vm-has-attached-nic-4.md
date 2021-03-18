<properties
	  pageTitle="Check if VM has attached NIC"
	  description="Check if VM has attached NIC"
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
	  articleId="bca3b855-549f-4d6d-acc0-74c8f813d891"
	  ownershipId="Azure_Security_Security_Center"
/>

# Check if VM has attached NIC

1. Make sure the NIC is attached to the VM with either public or private IP addresses. 
2. Please refer to [NIC attached to VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface)
3. JIT operates by creating Allow and Deny rules to the NSG. 
4. All VM's Netwroking must have both in order to be protected by Security Center JIT.

