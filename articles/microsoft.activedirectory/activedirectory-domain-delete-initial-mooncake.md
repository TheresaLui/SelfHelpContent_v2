<properties	
    pageTitle="I want to delete the initial .omschina.cn domain"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
	ms.author="curtand"
    displayOrder="40"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain,domain_directory"
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="activedirectory-domain-delete-initial-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I want to delete the initial .omschina.cn domain

## **Recommended Steps**

1. To delete the existing .omschina.cn domain, you must first delete the tenant instance you have created. Before you can delete the tenant, you must remove all users, groups and applications, and cancel your Azure and or Office 365 subscriptions. [Learn more](https://support.microsoft.com/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365).

2. If you have mistakenly created an Azure AD tenant with an initial .omschina.cn domain such as **myname.omschina.cn** and wish to update it to a friendlier company name like **contoso.omschina.cn**, you can configure a new Azure AD tenant and associate your subscriptions with the targeted tenant. [Learn more](https://support.microsoft.com/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365).

## **Recommended Documents**

* [Initial and custom domain names](https://docs.azure.cn/active-directory/users-groups-roles/domains-manage#initial-and-custom-domain-names)
* [Domain names in Azure AD and other Microsoft Online Services](https://docs.azure.cn/active-directory/users-groups-roles/domains-manage#domain-names-in-azure-ad-and-other-microsoft-online-services)

