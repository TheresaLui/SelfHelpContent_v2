<properties
pageTitle="Azure AD Connect detected a service busy error"
	description="Azure AD Connect detected a service busy error"
	infoBubbleText="Azure AD Connect detected a service busy error"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_Server_Busy"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Azure AD Connect detected a service busy error
<!--issueDescription-->
Azure AD Connect detected a service busy error. This could be because the service encountered an error while processing, reading and writing data in your Azure Active Directory. One possible reason could be the sync engine is being throttled due to high number of write operations.
<!--/issueDescription-->

## **Recommended Steps**

Please ensure that your sync cycle interval is configured to repeat at the default supported frequency (30 minutes). Running sync cycles too frequently can result in sync engine being throttled by Azure AD during the export operation, causing the export to fail temporarely.

This condition will usually clear automatically during the next sync cycle.



