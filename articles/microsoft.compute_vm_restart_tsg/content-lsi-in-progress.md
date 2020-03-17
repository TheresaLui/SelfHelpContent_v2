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
	cloudEnvironments="public"
	articleId="d9575991-a3a8-4f7a-924f-9742a6dcb9af"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if an LSI is in progress

* In some cases, there might be an existing LSI(Live Site Incident) occurred at the affected morment. 
* If you can find that LSI, you can deliver the issue shortly to the customer. 
* When checking LSIs, ASC will show you the service impact that the subscription has/is feeling recently
* In ASC, under Resource Explorer, Select the Virtual Machine customer request investigation;
* Select Health Tab
* Analyze the following components for more information 
   * VM Availability Impacts
   * Disk Availability Impacts
   * Service Impacting Events 
