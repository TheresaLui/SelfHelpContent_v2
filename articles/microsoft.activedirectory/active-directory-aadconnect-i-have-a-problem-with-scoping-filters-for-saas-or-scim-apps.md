<properties
	pageTitle="I have a problem with scoping filters for SaaS or SCIM apps"
	description="I have a problem with scoping filters for SaaS or SCIM apps"
	infoBubbleText="I have a problem with scoping filters for SaaS or SCIM apps"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684518"
	productPesIds="16666"
	articleId="97866ec6-a7a4-4b36-ab81-eacea79c16dc"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>


# I have a problem with scoping filters for SaaS or SCIM apps

## **Recommended Steps**

Please select one of the below options to learn more about scoping filters for SaaS or SCIM apps or to troubleshoot problems:

 * [I have a problem with configuring scoping filters for SaaS or SCIM apps](i-have-a-problem-with-mapping-attributes-for-saas-or-scim-apps)
 * [I want to learn more about automating user provisioning to SaaS or SCIM apps](https://docs.microsoft.com/azure/active-directory/manage-apps/customize-application-attributes)
 * [I want to learn more about integrating SaaS apps with Azure AD](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list)

### I have a problem with configuring scoping filters for SaaS or SCIM apps

* **Scoping filters** tell the provisioning service which users and groups in the source system should be provisioned and/or deprovisioned to the target system. There are two aspects to scoping filters that are evaluated together that determine who is in scope for provisioning:

	* **Filter on attribute values** - The "Source Object Scope" menu in the attribute mappings allows filtering on specific attribute values. For example, you can specify that only users with a "Department" attribute of "Sales" should be in scope for provisioning. For more information, see [Using scoping filters](https://docs.microsoft.com/azure/active-directory/manage-apps/define-conditional-rules-for-provisioning-user-accounts).
	* **Filter on assignments** - The "Scope" menu in the Provisioning > Settings section of the Azure portal allows you to specify whether only "assigned" users and groups should be in scope for provisioning, or if all users in the Azure AD directory should be provisioned. For information on "assigning" users and groups, see [Assign a user or group to an enterprise app in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/assign-user-or-group-access-portal).

The Azure AD user provisioning service logs all operations it performs during synchronization, and this includes the results of all user assignment and scoping filter operations. To view these logs, follow the steps recommended at [Provisioning audit logs](https://docs.microsoft.com/azure/active-directory/manage-apps/check-status-user-account-provisioning#provisioning-audit-logs).

## **Recommended Documents**

* [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-does-automatic-provisioning-work)
* [Customizing User Provisioning Attribute-Mappings for SaaS Applications in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/customize-application-attributes)
* [Tutorials for integrating SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list)
