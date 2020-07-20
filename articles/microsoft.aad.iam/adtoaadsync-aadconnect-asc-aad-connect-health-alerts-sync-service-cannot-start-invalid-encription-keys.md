<properties
pageTitle="Microsoft Azure AD Sync Windows service cannot start due to invalid encryption keys"
	description="Microsoft Azure AD Sync Windows service cannot start due to invalid encryption keys"
	infoBubbleText="Microsoft Azure AD Sync Windows service cannot start due to invalid encryption keys"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_Sync_Service_Cannot_Start_Invalid_Encryption_Keys"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Microsoft Azure AD Sync Windows service cannot start due to invalid encryption keys
<!--issueDescription-->
Microsoft Azure AD Sync Windows service cannot start due to invalid encryption keys. As a result data will not be synchronized between your directories.
<!--/issueDescription-->

## **Recommended Steps**
If you change the Azure AD Connect sync service account password, the Synchronization Service will not be able start correctly until you have abandoned the encryption key and reinitialized the Azure AD Connect sync service account password.
