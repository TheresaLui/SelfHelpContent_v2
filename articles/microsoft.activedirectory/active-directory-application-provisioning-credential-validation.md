<properties
	pageTitle="Problems with credential validation while configuring user provisioning to an application"
	description="Problems with credential validation while configuring user provisioning to an application"
	infoBubbleText="Problems with credential validation while configuring user provisioning to an application"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="asmalser-msft"
	ms.author="asmalser"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629801"
	productPesIds="16666"
	articleId="8d591007-b474-4b63-9f3e-451f17322ef4"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problems with credential validation while configuring user provisioning to an application

In order for automated user provisioning to work, Azure AD requires valid credentials that allow it to connect to a user management API provided by the application. If the Azure portal is returning an error upon saving the credentials, as described in [How do I set up automatic user provisioning to an application](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-do-i-set-up-automatic-provisioning-to-an-application), then follow the recommended steps below. 

## **Recommended Steps**

1. First, confirm that you have met all of the prerequisites for provisioning users to your application, have set up the administrative credentials in the app with the correct level of permissions, and that you are entering them into the Azure portal in the prescribed format. For more information, see the tutorial specific to your application at [Tutorials for integrating SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list).

2. Next, check to ensure any public endpoint URLs you are entering in the portal are valid. Open a web browser, and browse to the URL you are entering. If the web browser returns an HTTP 404 "Not Found" response, then the URL is likely invalid and the Azure AD user provisioning will not be able to connect to it either.

3. Finally, if you have already set up Azure AD single sign-on to the application, there is a known issue with key storage limitations that may be affecting you. For more information and a work-around, see: [Problem saving administrator credentials while configuring user provisioning to an Azure Active Directory Gallery application](https://docs.microsoft.com/azure/active-directory/manage-apps/application-provisioning-config-problem-storage-limit). 

## **Recommended Documents**

* [Automate user provisioning and deprovisioning to SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/user-provisioning#how-does-automatic-provisioning-work)
* [Tutorials for integrating SaaS applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list)


