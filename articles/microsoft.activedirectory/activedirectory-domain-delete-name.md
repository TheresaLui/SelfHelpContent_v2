<properties
    pageTitle="I can't delete my domain name"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
	ms.author="curtand"
    displayOrder="4295"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain,domain_directory"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="f77b8ca9-1dd7-42ea-a912-408ad2b6ea7b"
	ownershipId="AzureIdentity_User"
/>

# I can't delete my domain name

## **Recommended steps**

1. Ensure that you have removed all users, groups and applications utilizing the domain name you are trying to remove. There cannot be any dependencies on the domain name; for example, such as the User Principal Name (UPN) cannot contain the custom domain name. If an Admin’s account is admin@contoso.com it will fail you are trying to delete “contoso.com”, instead use an account like admin@contoso.onmicrosoft.com. Learn more in [Unable to remove a custom domain](https://support.microsoft.com/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365). 

2. If you have multiple sub-domains in your tenant, you will need to remove each one before you can delete the root domain. For example, if you have **na.contoso.com** and **emea.contoso.com**, you must delete the child domains before you can delete the parent domain **contoso.com**. [Learn more](https://support.microsoft.com/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365).

## **Recommended documents**

* [Add a custom domain name in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain)
* [PowerShell for deleting a domain](https://docs.microsoft.com/powershell/msonline/v1/remove-msoldomain)
