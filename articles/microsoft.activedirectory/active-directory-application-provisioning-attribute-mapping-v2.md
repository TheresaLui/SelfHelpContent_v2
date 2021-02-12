<properties
	pageTitle="Problems with attribute mappings while provisioning users to an application"
	description="Problems with attribute mappings while provisioning users to an application"
	infoBubbleText="Problems with attribute mappings while provisioning users to an application"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="ArvindHarinder1"
	ms.author="ArvindHarinder1"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684520"
	productPesIds="16666"
	articleId="3472d233-5761-4e03-9dc5-c987a5015bea"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with attribute mappings while provisioning users to an application

In the Azure AD user provisioning service, attribute mappings allow you to map how user attribute values in Azure AD (ex: first name, last name) flow into the user attributes present in other system's user repositories.

## **Recommended Steps**

* Use the [on-demand provisioning](https://docs.microsoft.com/azure/active-directory/app-provisioning/provision-on-demand) capability to provision a user and get detailed diagnostics about the steps taken.
* For documentation on how to configure attribute mappings in the Azure AD user provisioning service, see [Customizing User Provisioning Attribute-Mappings for SaaS Applications in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/customize-application-attributes)
* Occasionally, the provisioning configuration tutorials for selected applications may make recommendations or list known issues specific to your application. For more information, find the tutorial specific to your application at [Tutorials for integrating SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list).


## **Recommended Documents**

* [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-does-automatic-provisioning-work)
* [Customizing User Provisioning Attribute-Mappings for SaaS Applications in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/customize-application-attributes)
* [Tutorials for integrating SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list)
