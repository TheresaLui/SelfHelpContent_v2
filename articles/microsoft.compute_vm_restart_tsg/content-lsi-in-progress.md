<properties
	pageTitle="Check if an LSI is in progress"
	description="Check if an LSI is in progress"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d9575991-a3a8-4f7a-924f-9742a6dcb9af"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if an LSI is in progress

1. In some cases, there might be an existing LSI(Live Site Incident) that occurred at the affected moment of the VM Restart. 
2. If you can find that LSI, you can deliver the issue quickly to the customer. 
3. When checking LSIs, ASC will show you the service impact on the subscription
4. In ASC, under Resource Explorer, Select the Virtual Machine customer request investigation;
5. Select Health Tab
   1. Analyze the following components for more information 
   2. VM Availability Impacts
   3. Disk Availability Impacts
   4. Service Impacting Events 
