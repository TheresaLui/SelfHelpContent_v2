<properties
    pageTitle="I'm having a problem deleting my Azure AD tenant"
    description="I'm having a problem deleting my Azure AD tenant"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    ms.author="elkuzmen"
    displayOrder="43"
    supportTopicIds="32565595, 32565596"
    selfHelpType="resource"
    resourceTags="directory_delete,directory_overview"
    productPesIds="16578"
    cloudEnvironments="MoonCake"
    articleId="activedirectory-directory-deletetenantdependenciestshooter-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I'm having a problem deleting my Azure AD tenant

## **Recommended Steps**

To delete an Azure AD tenant, you must first remove or transfer any associations to your custom domain names in your directory. This includes any users, groups, or applications, and any Azure or  Office 365 subscriptions in the directory. For guidance on adding an existing subscription to an Azure AD tenant, refer to [Associate or add an Azure subscription to your Azure Active Directory tenant](https://docs.azure.cn/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory). Deleting an Azure AD tenant is irreversible. Any data homed in the directory is permanently deleted. Learn more about [deleting a directory](https://docs.azure.cn/active-directory/fundamentals/active-directory-whatis).

1. Ensure that you are are the global administrator for the directory and that you are the only user in the directory. Any other users must be deleted before the directory can be deleted. If users are synchronized from on-premises, then sync will need to be turned off, and the users must be deleted in the cloud directory by using the Azure portal or PowerShell.
2. There can be no applications in the directory. Any applications must be deleted before the directory can be deleted.
3. There can be no subscriptions for any Microsoft Online Services such as Microsoft Azure, Office 365, or Azure AD Premium associated with the directory. For more information about Azure subscriptions, see [Cancel your Azure subscription](https://docs.azure.cn/billing/billing-how-to-cancel-azure-subscription).
4. Ensure that if you are signed in with a work or school account, you must not be attempting to delete your home directory. For example, if you are is signed in as joe@contoso.omschina.cn, you cannot delete the directory that has contoso.omschina.cn as its default domain.  
5. No multi-factor authentication providers can be linked to the directory.  

## **Recommended Documents**

* [Deleting Users from Azure Active Directory](https://docs.azure.cn/active-directory/fundamentals/add-users-azure-active-directory)
* [Removing applications in the directory](https://docs.azure.cn/active-directory/develop/quickstart-register-app#removing-an-application)
* [Transfer ownership of an Azure subscription to another account](https://docs.azure.cn/billing/billing-subscription-transfer)
* [Additional information on deleting an Azure AD](https://docs.azure.cn/active-directory/fundamentals/active-directory-whatis#how-can-i-delete-an-azure-ad-directory)
