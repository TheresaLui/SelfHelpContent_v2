<properties
	pageTitle="The provisioning service is slow or in a quarantined state"
	description="The provisioning service is slow or in a quarantined state"
	infoBubbleText="The provisioning service is slow or in a quarantined state"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="rodejo"
	ms.author="rodejor"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684524"
	productPesIds="16666"
	articleId="2f95fd80-eae3-4a65-9202-f41bfcef2152"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# The provisioning service is slow or in a quarantined state

The Azure AD user provisioning service continuously synchronizes user account data from Azure AD to target applications, typically on 40 minute sync cycle intervals. However, the time it takes to complete a sync cycle depends on what type of cycle it is (initial sync or incremental sync), and how much user data needs to be processed.

A provisioning job can also go into a "quarantine" state, which means that the frequency of sync execution has been reduced due to a high volume of errors.

These concepts are described in detail at [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#what-happens-during-provisioning).

For recommended steps dealing with slow provisioning jobs and quarantine, see the appropriate sections below.

## **Recommended Steps**

**Slow Provisioning Jobs**

1. Use the [on-demand provisioning](https://docs.microsoft.com/azure/active-directory/app-provisioning/provision-on-demand) capability to provision a user and get detailed diagnostics about the steps taken.
2. Pereodically restart provisioning to catch any users that were missed in a previous provisioning cycle
3. For detailed information on how to estimate the time it will take to complete a user provisioning cycle, see [How long will it take to provision users?](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-long-will-it-take-to-provision-users)

**Quarantined provisioning jobs**

1. For information on why provisioning jobs can go into quarantine, see [What happens during automatic provisioning?](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#what-happens-during-provisioning)
2. If the provisioning job has gone into quarantine due to a high volume of errors (error code = `EntryLevelError`), check the [provisioning audit logs](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning#provisioning-audit-logs) to view the details of these errors.

## **Recommended Documents**

* [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-does-automatic-provisioning-work)
* [Reporting on automatic user provisioning](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning)
