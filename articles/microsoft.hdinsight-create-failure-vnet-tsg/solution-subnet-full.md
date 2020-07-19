<properties
	pageTitle="Subnet full"
	description="Subnet full"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="90734a84-6f5c-4391-8951-dd9bcadeec23"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Subnet full

<!--issueDescription-->

We have checked the cluster and it seems that cluster creation failure is due to full subnet

To resolve the issue:

1. Check if your subnet has unused resources, remove the unused resource and recreate the cluster  
2. If your subnet was small, increase the subnet range and recreate the cluster

<!--/issueDescription-->

## Recommended documents

1. [Virtual Networks Overview](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview)