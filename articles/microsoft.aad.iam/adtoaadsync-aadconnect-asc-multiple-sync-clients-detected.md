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

Validate your setup. If you have multiple sync clients synchronizing by mistake, make sure that **only one** client is **actively exporting** changes to Azure AD.

For all other servers, enable [staging mode](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-staging-server),  or decommission them by uninstalling Azure AD Connect if they are no longer required.
