<properties
	  pageTitle="Test to see if other VMs in the same subnet can be reached."
	  description="Test to see if other VMs in the same subnet can be reached."
      service="Microsoft.network"
      resource="Microsoft.network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="9aaa6c9e-471e-4610-8c8d-3d89dc59e2cb"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Test to see if other VMs in the same subnet can be reached.

You will occasionally run into situations where although there are multiple resources in the same subnet that should be governed by the same routes and security policies there may be one resource that is having issues. 

#Recommended Steps

	1. Test the scenario using a different VM in the same subnet as the new destination. (PSPing is recommended )
	
#Reccommended Documents
?
	1. (PsPing) [https://docs.microsoft.com/en-us/sysinternals/downloads/psping]

