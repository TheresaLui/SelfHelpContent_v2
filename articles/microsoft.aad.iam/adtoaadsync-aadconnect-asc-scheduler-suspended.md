<properties
	pageTitle="AAD Connect synchronization cycle is suspended"
	description="AAD Connect synchronization cycle is suspended"
	infoBubbleText="AAD Connect synchronization cycle is suspended. See details on the right."
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="aditis"
	ms.author="sahaaditi"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_SynchronizationCycleSuspended"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# The Azure AD Sync scheduler is suspended
<!--issueDescription-->
We have detected the synchronization cycle is suspended on server(s) for your tenant.
<!--/issueDescription-->

When the synchronization cycle is suspended on an Azure AD Connect server, the synchronization process will no longer synchronize data between the on-premises Active Directory and Azure Active Directory. The scheduler is suspended by Connect during an upgrade to temporarily block the scheduler from running. Normally, the upgrade process will re-enable the scheduler to run as scheduled after the upgrade process completes. Under some circumstances this does not happen correctly, causing the scheduler to be suspended.

You need to re-enable the scheduler to synchronize data again.

## **Recommended Steps**

* Run the following cmdlet on each affected Azure AD Connect server: `Set-ADSyncScheduler -SyncCycleEnabled $true`

	This cmdlet will enable the synchronization cycle and synchronization will resume at the configured interval.

## **Recommended Documents**

* [Active Directory Connect Sync Scheduler](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#overview)
