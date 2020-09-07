<properties
	pageTitle="Problems while configuring Workday to AD User Provisioning service"
	description="Problems while configuring Workday to AD User Provisioning service"
	infoBubbleText="Problems while configuring Workday to AD User Provisioning service"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cmmdesai"
	ms.author="chmutali"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684510"
	productPesIds="16666"
	articleId="4f779b64-8c57-4471-bd22-3f3312f46702"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Problem configuring the provisioning service

In order for automated user provisioning to work, Azure AD requires valid credentials that allow it to connect to Workday Web Services API. Further the *Test Connection* button on the **Workday to AD User Provisioning app** also validates if it is able to connect to the Azure AD Connect Provisioning Agent associated with the AD Domain. If the Azure portal is returning an error upon saving the credentials, then follow the recommended steps below.

## **Recommended Steps**

1. First, confirm that you have configured Workday Integration System User account as stated in the tutorial section [Configure integration system user in Workday](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial#configure-integration-system-user-in-workday)
1. Next, confirm that the Azure AD Connect Provisioning Agent Service is up and running on your on-premises Windows server using the Services Management Console. You can also check the status of the agent in the Azure portal by clicking the *View on-premises agents* button.
1. Ensure that you are entering the value for "Workday Username" field using the format **username@workday-tenant-name**. If the workday-tenant-name is missing, Workday authentication fails.
1. If you are configuring the integration with Workday implementation tenant, please note the scheduled downtime hours of your Workday tenant. Workday has scheduled down time for its implementation tenants over weekends (usually from Friday evening to Saturday morning) and connectivity failures during this downtime window is a known issue that auto-resolves as soon as the implementation tenants are back online.
1. In rare cases, you may also see this error if the password of the Integration System User changed due to tenant refresh or if the account is in locked or expired state. Please check the status of the Integration System user with your Workday administrator.

## **Recommended Documents**

* [Tutorial: Configure Workday for automatic user provisioning](https://docs.microsoft.com/azure/active-directory/saas-apps/workday-inbound-tutorial)
