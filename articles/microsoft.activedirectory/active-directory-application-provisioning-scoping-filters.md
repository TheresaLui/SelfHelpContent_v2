<properties
	pageTitle="Problems with configuring scoping filters for user provisioning to an application"
	description="Problems with configuring scoping filters for user provisioning to an application"
	infoBubbleText="Problems with configuring scoping filters for user provisioning to an application"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="asmalser-msft"
	ms.author="asmalser"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629804"
	productPesIds="16666"
	articleId="639b0be2-d484-4d82-8544-287888df024b"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with configuring scoping filters for user provisioning to an application

* **Scoping filters** tell the provisioning service which users and groups in the source system should be provisioned and/or deprovisioned to the target system. There are two aspects to scoping filters that are evaluated together that determine who is in scope for provisioning:

    * **Filter on attribute values** - The "Source Object Scope" menu in the attribute mappings allows filtering on specific attribute values. For example, you can specify that only users with a "Department" attribute of "Sales" should be in scope for provisioning. For more information, see [Using scoping filters](https://docs.microsoft.com/azure/active-directory/manage-apps/define-conditional-rules-for-provisioning-user-accounts).

    * **Filter on assignments** - The "Scope" menu in the Provisioning > Settings section of the Azure portal allows you to specify whether only "assigned" users and groups should be in scope for provisioning, or if all users in the Azure AD directory should be provisioned. For information on "assigning" users and groups, see [Assign a user or group to an enterprise app in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/assign-user-or-group-access-portal).

To troubleshoot scoping filters, follow the recommended steps below.

## **Recommended Steps**

* The Azure AD user provisioning service logs all operations it performs during synchronization, and this includes the results of all user assignment and scoping filter operations. To view these logs, follow the steps recommended at [Provisioning audit logs](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning#provisioning-audit-logs).


## **Recommended Documents**

* [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-does-automatic-provisioning-work)

* [Tutorials for integrating SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list)

* [Provisioning audit logs](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning#provisioning-audit-logs)
