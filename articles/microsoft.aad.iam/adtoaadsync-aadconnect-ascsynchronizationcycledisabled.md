<properties
	pageTitle="AAD Connect synchronization cycle is disabled"
	description="AAD Connect synchronization cycle is disabled"
	infoBubbleText="AAD Connect synchronization cycle is disabled. See details on the right."
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="aditis"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_SynchronizationCycleDisabledd"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>
# The Azure AD Sync scheduler is disabled
<!--issueDescription-->
## The Azure AD Sync scheduler is disabled
We have detected synchronization cycle is disabled on server(s) for your tenant.

When the synchronization cycle is disabled on an Azure AD Connect server, the synchronization process will no longer synchronize data between the on-premises Active Directory and Azure Active Directory. Please enable the synchronization cycle on each affected Azure AD Connect server.
<!--/issueDescription-->
## **Recommended steps**
To enable the synchronization cycle, execute the following PowerShell cmdlet on the AADConnect server: 

`Set-ADSyncScheduler -SyncCycleEnabled $true` 

This cmdlet will enable the synchronization cycle and synchronization will resume at the configured interval.

For more information about stopping, starting, enabling and disabling the synchronization cycle please refer to this article: [https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#overview ](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#overview) 
