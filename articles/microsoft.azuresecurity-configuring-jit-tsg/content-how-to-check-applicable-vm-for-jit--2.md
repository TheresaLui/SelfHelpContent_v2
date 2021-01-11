<properties
	  pageTitle="How to check applicable VM for JIT "
	  description="How to check applicable VM for JIT "
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
	  articleId="d339a961-2aef-468b-85b0-f4c0648feb8b"
	  ownershipId="Azure_Security_Security_Center"
/>

# How to check applicable VM for JIT 

Conditions for a VM to be "recommended" for JIT configuration

1. The VM must be ARM (classic is not currently supported).
2. The VM must have an attached NIC.
3. The VM attached NIC has an NSG attached to it.
