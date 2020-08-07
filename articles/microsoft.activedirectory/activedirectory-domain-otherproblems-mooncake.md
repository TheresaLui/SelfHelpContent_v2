<properties
    pageTitle="I still have other problems related to domain name management"
    description="Azure Active Directory domains troublehooter"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="curtand"
	ms.author="curtand"
    displayOrder="38"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_domain"
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="activedirectory-domain-otherproblems-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I still have other problems related to domain name management
 
## **Recommended Steps** 

1.	Ensure that your domain name hasn’t already been configured in another Azure AD tenant or in Office 365. If you have already configured your domain name in Office 365 and are trying to add it to another Azure AD tenant, verification will fail. If that happens, remove it from the Azure AD tenant where the domain name is already verified and add it to your Azure AD tenant. The same custom domain name cannot be verified by two different tenants.
2.	If someone in your organization used self-service sign-up for PowerBI or Rights Management Services (RMS),they may have created an unmanaged tenant. You can manage this tenant with [admin takeover](https://docs.azure.cn/active-directory/users-groups-roles/directory-self-service-signup) or can proceed to add the domain with force takeover option in [PowerShell](https://docs.microsoft.com/powershell/msonline/v1/confirm-msoldomain).
3.	If you are trying to configure a custom domain name for federated single sign-on, and you do not have ADFS set up, you must configure federation settings in your directory with the Azure AD Connect tool to use your custom domain name. 
4.	If you are trying to delete an Azure AD tenant, there can be no active subscriptions for any Microsoft Online Services such as Microsoft Azure, Office 365, or Azure AD Premium associated with the tenant you're trying to delete. Transfer your subscriptions or expedite cancellation of active subscriptions by using [Azure Support and Billing](https://support.office.com/article/Contact-Office-365-for-business-support-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b).

## **Recommended Documents**

* [Add subdomains of a custom domain name](https://docs.azure.cn/active-directory/users-groups-roles/domains-manage#add-subdomains-of-a-custom-domain) 
* [Use PowerShell or Graph API to manage domain names](https://docs.azure.cn/active-directory/users-groups-roles/domains-manage#use-powershell-or-graph-api-to-manage-domain-name)