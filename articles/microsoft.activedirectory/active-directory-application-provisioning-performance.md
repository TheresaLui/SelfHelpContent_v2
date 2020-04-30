<properties
	pageTitle="Problems with user provisioning to an application being slow or in quarantine"
	description="Problems with user provisioning to an application being slow or in quarantine"
	infoBubbleText="Problems with user provisioning to an application being slow or in quarantine"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="asmalser-msft"
	ms.author="asmalser"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629807"
	productPesIds="16666"
	articleId="3eefc8c1-c360-495a-bfe0-ea51ac686ddd"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with user provisioning to an application being slow or in quarantine

The Azure AD user provisioning service perpetually synchronizes user account data from Azure AD to target applications, typically on 40 minute sync cycle intervals. However, the time it takes to complete a sync cycle depends on what type of cycle it is (initial sync or incremental sync), and how much user data needs to be processed.

A provisioning job can also go into a "quarantine" state, which means that the frequency of sync execution has been reduced due to a high volume of errors.

These concepts are described in detail at [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#what-happens-during-provisioning).

For recommended steps dealing with slow provisioning jobs and quarantine, see the appropriate sections below.

## **Recommended Steps**

**Slow Provisioning Jobs**

* For detailed information on how to estimate the time it will take to complete a user provisioning cycle, see [How long will it take to provision users?](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-long-will-it-take-to-provision-users)

**Quarantined provisioning jobs**

1. For information on why provisioning jobs can go into quarantine, see [What happens during automatic provisioning?](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#what-happens-during-provisioning)
2. If the provisioning job has gone into quarantine due to a high volume of errors (error code = `EntryLevelError`), check the [provisioning audit logs](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning#provisioning-audit-logs) to view the details of these errors.

## **Recommended Documents**

* [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-does-automatic-provisioning-work)
* [Reporting on automatic user provisioning](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning)
