<properties
pageTitle="AAD Connect server(s) are running low in memory"
	description="AAD Connect server(s) are running low in memory"
	infoBubbleText="AAD Connect server(s) are running low in memory"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_OutOfMemory"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# AAD Connect server(s) are running low in memory
<!--issueDescription-->
This tenant has server(s) which are running low in memory. Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
Determine the cause of the memory pressure. If sync engine is using up the memory, it could be that the server is under-resourced or the sync engine is taking way too much memory than it should. If sync engine is taking more memory than it should, it will need deeper investigation, please open a Support Request. For any other case, please add aditional memory.
