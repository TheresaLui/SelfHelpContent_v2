<properties
    pageTitle="Synchronization Service is started but there is no synchronization activity"
    description="Synchronization Service is started but there is no synchronization activity"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="224"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect,directory_overview"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="de1b995a-6d58-444a-a2f1-9ec874dd2d75"
	ownershipId="AzureIdentity_User"
/>

# Synchronization Service is started but there is no synchronization activity

## **Recommended steps**
The Azure AD Connect Synchronization Service appears to be running in the Windows Service Control Manager but there is no sychronization activity. Common root causes include the following:

* The Azure Azure Connect wizard is currently open on the Azure AD Connect server. If you start the installation wizard, the scheduler is temporarily suspended until the wizard is closed. For details about this behavior, refer to article section [Azure AD Connect sync: Scheduler - Scheduler and installation wizard](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler#scheduler-and-installation-wizard).

* The Azure AD Connect sync scheduler is currently disabled. To verify the status and start the sync scheduler, refer to the steps in article [Azure AD Connect sync: Scheduler](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler).

* The Azure AD Connect server is currently in staging mode. When the Connect server is in staging mode, it will be active for import and synchronization. However, it will not run any exports. For details about staging mode, refer to article section [Azure AD Connect sync: Operational tasks and consideration - Staging mode](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations#staging-mode).

## **Recommended documents**
* [Azure AD Connect sync: Scheduler](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-scheduler)  
* [Azure AD Connect sync: Operational tasks and consideration](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-operations)  
