<properties
pageTitle="Azure AD Connect sync service is not running. The Service account failed to authenticate."
	description="Azure AD Connect sync service is not running. The Service account failed to authenticate."
	infoBubbleText="Azure AD Connect sync service is not running. The Service account failed to authenticate."
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_Sync_Service_Not_Running_Service_Account_Failed_To_Authenticate"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Azure AD Connect sync service is not running. The Service account failed to authenticate.
<!--issueDescription-->
The Sync service is not running due to expired Windows Service account credentials. As a result, objects will not synchronize with Azure Active Directory.
<!--/issueDescription-->

## **Recommended Steps**

- Verify if the service account used to run synchronization service exists in your Active Directory
- Verify that the service account password has not expired. It is recommended that the account should be configured with "password never expires" option.
- Ensure the service account has right permissions to log into Windows. Check if any group policy is changing the permissions.
