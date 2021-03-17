<properties
pageTitle="Sync service account does not have permissions to update AD Objects"
	description="Sync service account does not have permissions to update AD Objects"
	infoBubbleText="Sync service account does not have permissions to update AD Objects"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_Permission_Issue"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Sync service account does not have permissions to update AD Objects
<!--issueDescription-->
The service account used for synchronization does not have permissions to update AD Objects. As a result some of the objects with the Active Directory may not be synchronized with Azure Active Directory.
<!--/issueDescription-->

## **Recommended Steps**

Please perform the following actions:
- Verify if the service account used to run synchronization service exists in your Active Directory
- Verify that the service account password has not expired. It is recommended that the account should be configured with "password never expires" option.
- Verify that the account has the required permissions to access your Active Directory objects
- Ensure the service account has right permissions to log into Windows. Check if any group policy is changing the permissions.
