<properties
	pageTitle="AAD Connect synchronization cycle is disabled"
	description="AAD Connect synchronization cycle is disabled"
	infoBubbleText="AAD Connect synchronization cycle is disabled. See details on the right."
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="aditis"
	ms.author="sahaaditi"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_SynchronizationCycleDisabled"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="1666"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# The Azure AD Sync scheduler is disabled
<!--issueDescription-->
We have detected that the synchronization cycle is disabled on server(s) for your tenant.
<!--/issueDescription-->

When the synchronization cycle is disabled on an Azure AD Connect server, the synchronization process will no longer synchronize data between the on-premises Active Directory and Azure Active Directory. Please enable the synchronization cycle on each affected Azure AD Connect server.

## **Recommended Steps**

* Execute the following PowerShell cmdlet on the Azure AD Connect server: `Set-ADSyncScheduler -SyncCycleEnabled $true`

	This cmdlet will enable the synchronization cycle and synchronization will resume at the configured interval.

## **Recommended Documents**

* [Active Directory Connect Sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#overview)
