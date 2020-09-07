<properties
    pageTitle="I can't delete my domain name"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
	ms.author="curtand"
    displayOrder="39"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain,domain_directory"
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="activedirectory-domain-delete-name-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I can't delete my domain name

## **Recommended Steps**

1. Ensure that you have removed all users, groups and applications utilizing the domain name you are trying to remove. There cannot be any dependencies on the domain name. For example, such as the User Principal Name (UPN) cannot contain the custom domain name. If an admin's account is admin@contoso.cn it will fail you are trying to delete "contoso.cn", instead use an account like admin@contoso.omschina.cn. Learn more in [Unable to remove a custom domain](https://support.microsoft.com/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365). 
2. If you have multiple subdomains in your tenant, you will need to remove each one before you can delete the root domain. For example, if you have **na.contoso.cn** and **emea.contoso.cn**, you must delete the child domains before you can delete the parent domain **contoso.cn**. [Learn more](https://support.microsoft.com/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365).

## **Recommended Documents**

* [Add a custom domain name in Azure AD](https://docs.azure.cn/active-directory/fundamentals/add-custom-domain)
* [PowerShell for deleting a domain](https://docs.microsoft.com/powershell/msonline/v1/remove-msoldomain)
