<properties
	pageTitle="Product Engineering Escalation"
	description="Product Engineering Escalation"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="92f844fc-0c21-4031-ba8c-1b346c6fedfb"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Product Engineering Escalation
<!--issueDescription-->
**INTERNAL ESCALATION PROCEDURE**
1. Use MSSolve to Create a CRI.
2. If MSSolve is failing use the [AzureRT ICM Template](https://aka.ms/CRI-AzureRT) and include a note the MSSolve was not an option. 
3. Follow the typical guidelines Sev1 & SEV2 go through WASU/PG, SEV3 - SEV4 go through EEE.
4. Case Coding
    1. If customer had to perform Commit/Abort operation to unblock the issue:
Root cause - Azure Storage\Storage Account Management\Account deletion issue\Other
    2. If Engineering team was engaged and bug is confirmed:
Root cause - Azure Storage\Storage Account Management\Account deletion issue\Product bug
<!--/issueDescription-->
