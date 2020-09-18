<properties
pageTitle="Scheduler maintenance tasks are disabled"
	description="Scheduler maintenance tasks are disabled"
	infoBubbleText="Scheduler maintenance tasks are disabled"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_MaintenanceDisabled"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Scheduler maintenance tasks are disabled
<!--issueDescription-->
We have detected scheduler maintenance tasks are disabled. When this happens, keys and certificates are not renewed for Password Reset and Device Registration Service(DRS). Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
When maintenance tasks are disabled on a AAD Connect server, keys and certificates are not renewed for Password Reset and Device Registration Service(DRS).

To enable the maintenance tasks, execute the following powershell cmdlet on each server listed above: `Set-ADSyncScheduler -MaintenanceEnabled $true`
