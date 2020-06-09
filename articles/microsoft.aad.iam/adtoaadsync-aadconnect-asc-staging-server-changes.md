<properties
pageTitle="Staging server(s) status changed"
	description="Staging server(s) status changed"
	infoBubbleText="Staging server(s) status changed"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_Staging_Server_Changes"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
	cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Staging server(s) status changed
<!--issueDescription-->
This tenant has machine(s) configured as staging servers and now are active (or vice versa). Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
Please be aware that when staging mode is disabled, the AADConnect server starts exporting, enables password sync, and enables password writeback. The opposite happens when the staging mode is enabled.
