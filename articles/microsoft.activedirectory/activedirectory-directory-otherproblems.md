<properties
    pageTitle="I still have other problems deleting my Azure AD tenant"
    description="Azure Active Directory directory troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="elkuzmen"
    displayOrder="4299"
    selfHelpType="resource"
    supportTopicIds="32565596"
    resourceTags="directory_delete"
    productPesIds="14785,16578"
    cloudEnvironments="public"
    	articleId="02aafe9c-3938-489b-9481-ca8ffb1813ec"
/>

# I still have other problems deleting my Azure AD tenant

## **Recommended steps**

1. To delete an Azure AD, you need to be a Global Administrator on the directory. Ensure you are NOT signed in with an account that has the default directory such as contoso.onmicrosoft.com in the signed-in account, such as admin@contoso.onmicrosoft.com.
2. If there are any active applications in the directory, they must be removed before deletion can occur. Navigate to App registrations and remove the existing applications.
3. Ensure there are no active subscriptions for any Microsoft Online Services, such as Microsoft Azure, Office 365 or Azure AD Premium associated on the directory you are trying to delete. You must transfer your subscriptions or expedite cancellation of active subscriptions via Azure Support and Billing. Learn more on How to Cancel Office 365 and Azure subscriptions.
4. Check that there are no other active users in the directory besides yourself as the Global Administrator when attempting to delete the Azure AD. Remove any other active users, and any dependencies on a custom domain name in the tenant will also need to be removed, such as users created with admin@contoso.com.

## **Recommended documents**

* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)<br>
* [Add subdomains of a custom domain name](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#add-subdomains-of-a-custom-domain)<br>
* [Resource dependencies in Office 365 and Azure AD tenants](https://docs.microsoft.com/azure/active-directory/active-directory-licensing-directory-independence)<br>
* [Use PowerShell or Graph API to manage domain names](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal#use-powershell-or-graph-api-to-manage-domain-names)  