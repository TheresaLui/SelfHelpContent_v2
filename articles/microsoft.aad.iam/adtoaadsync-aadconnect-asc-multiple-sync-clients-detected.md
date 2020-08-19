<properties
pageTitle="Multiple sync clients detected"
	description="Multiple sync clients detected"
	infoBubbleText="Multiple sync clients detected"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_Multiple_Sync_Clients_Detected"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Multiple sync clients detected
<!--issueDescription-->
The following host machines are synchronizing to Azure AD directory: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
Please validate your setup. If you have multiple sync clients synchronizing by mistake, you need to make sure only one client synchronizes objects to their Azure AD directory.
You need to decommission other sync clients(s) by uninstalling Azure AD Connect from those host machines.
