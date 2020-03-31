<properties
    pageTitle="I still have other problems deleting my Azure AD tenant"
    description="Azure Active Directory directory troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    ms.author="elkuzmen"
    displayOrder="41"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_delete"
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="activedirectory-directory-otherproblems-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I still have other problems deleting my Azure AD tenant

## **Recommended Steps**

1. To delete an Azure AD, you need to be a Global Administrator on the directory. Ensure you are NOT signed in with an account that has the default directory such as contoso.omschina.cn in the signed-in account, such as admin@contoso.omschina.cn.
2. If there are any active applications in the directory, they must be removed before deletion can occur. Navigate to App registrations and remove the existing applications.
3. Ensure there are no active subscriptions for any Microsoft Online Services, such as Microsoft Azure, Office 365 or Azure AD Premium associated on the directory you are trying to delete. You must transfer your subscriptions or expedite cancellation of active subscriptions via Azure Support and Billing. Learn more on How to Cancel Office 365 and Azure subscriptions.
4. Check that there are no other active users in the directory besides yourself as the Global Administrator when attempting to delete the Azure AD. Remove any other active users, and any dependencies on a custom domain name in the tenant will also need to be removed, such as users created with admin@contoso.cn.

## **Recommended Documents**

* [Transfer ownership of an Azure subscription to another account](https://docs.azure.cn/billing/billing-subscription-transfer)
* [Add subdomains of a custom domain name](https://docs.azure.cn/active-directory/users-groups-roles/domains-manage#add-subdomains-of-a-custom-domain)
* [Use PowerShell or Graph API to manage domain names](https://docs.azure.cn/active-directory/users-groups-roles/domains-manage#use-powershell-or-graph-api-to-manage-domain-names)  