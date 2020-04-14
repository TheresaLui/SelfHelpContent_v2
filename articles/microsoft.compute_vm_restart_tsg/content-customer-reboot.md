<properties
	pageTitle="Check for customer initiated restarts and multiple restarts"
	description="Check for customer initiated restarts and multiple restarts"
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
	articleId="bb09c5a0-b99b-479f-b631-99a706a3d64f"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check for customer initiated restarts and multiple restarts

1. Check the customer’s case history in Service Desk to understand if the customer has been having a history of unexpected restarts lately. (Go to Customer -> View details and look at the "Support History" section)
2. Just in case, precheck the CRP operations on Azure Support Center (ASC) about whether the customer performed any reboot/deallocate & restart operaitons around the reported time. 

**Note:** If you've observed multiple restarts for this customer, then run each re-start through this troubleshooter as each restart may have different causes and mitigation. 