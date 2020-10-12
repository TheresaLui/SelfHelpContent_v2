<properties
pageTitle="Password Hash Synchronization has stopped working"
	description="Password Hash Synchronization has stopped working"
	infoBubbleText="Password Hash Synchronization has stopped working"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_PHS_Stopped_Working"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Password Hash Synchronization has stopped working
<!--issueDescription-->
Password Hash Synchronization has stopped. As a result passwords will not be synchronized with Azure Active Directory.
<!--/issueDescription-->

## **Recommended Steps**
Restart Microsoft Azure Active Directory Sync Services. Any synchronization operations that are currently running will be interrupted, therefore restart when no synchronization operation is in progress.
