<properties 
    pageTitle="I'm having a problem deleting my Azure AD tenant"
    description="I'm having a problem deleting my Azure AD tenant"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="ElizavetaKuzmenko"
    displayOrder="1875"
    supportTopicIds="32565595"
    selfHelpType="resource"
    resourceTags="directory_delete,directory_overview"
    productPesIds="14785" 
    cloudEnvironments="public"
    />
# I'm having a problem deleting my Azure AD tenant

## **Recommended steps**

To delete an Azure AD tenant, you must first remove any associations to your custom domain names in your directory, along with any users, groups, applications and your Azure and or Office 365 subscriptions in the directory. Deleting an Azure AD tenant is irreversible. Any data homed in the directory is permanently deleted. Learn more about [deleting a directory](https://docs.microsoft.com/azure/active-directory/active-directory-administer).

1. Ensure that you are are the global administrator for the directory and that you are the only user in the directory. Any other users must be deleted before the directory can be deleted. If users are synchronized from on-premises, then sync will need to be turned off, and the users must be deleted in the cloud directory by using the Azure portal or PowerShell. 
2. There can be no applications in the directory. Any applications must be deleted before the directory can be deleted.
3. There can be no subscriptions for any Microsoft Online Services such as Microsoft Azure, Office 365, or Azure AD Premium associated with the directory. For more information about Azure subscriptions, see [Cancel your Azure subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription).
4. Ensure that if you are signed in with a work or school account, you must not be attempting to delete your home directory. For example, if you are is signed in as joe@contoso.onmicrosoft.com, you cannot delete the directory that has contoso.onmicrosoft.com as its default domain.  
5. No multi-factor authentication providers can be linked to the directory.  
 
## **Recommended documents**

* [How Azure subscriptions are associated with Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory)

* [Deleting Users from Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)

* [Removing applications in the directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#removing-an-application)

* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)

* [Additional information on deleting an Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-administer#how-can-i-delete-an-azure-ad-directory) 