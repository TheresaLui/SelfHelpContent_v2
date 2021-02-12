<properties
pageTitle="Azure AD Connect Sync Service is not running"
	description="Azure AD Connect Sync Service is not running"
	infoBubbleText="Azure AD Connect Sync Service is not running"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_Sync_Service_Not_Running"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Azure AD Connect Sync Service is not running
<!--issueDescription-->
Microsoft Azure AD Sync Windows service is not running or could not start. As a result, objects will not synchronize with Azure Active Directory.
<!--/issueDescription-->

## **Recommended Steps**
Start Microsoft Azure Active Directory Sync Services:

- Click Start, click Run, type Services.msc, and then click OK
- Locate the Microsoft Azure AD Sync service, and then check whether the service is started. If the service is not started, right-click it, and then click Start.
