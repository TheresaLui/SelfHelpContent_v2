<properties
	pageTitle="Solutions to common problems"
	description="Azure Active Directory domains troublehooter"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="curtand"
	displayOrder="25"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="directory_domain"
	productPesIds=""
	cloudEnvironments="public"
/>

# Solutions to common problems

## I can't verify my domain name after I have added it to the Azure portal

### Recommended steps

1. Ensure that you have configured your TXT/MX record with your domain name registrar. [Learn more.](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#add-the-dns-entry-at-the-domain-name-registrar-for-the-domain)

2. If you have previously configured your domain name with another Azure AD tenant or Office 365 tenant, you will need to troubleshoot the domain from the existing tenant. [Learn more.](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain#troubleshooting)*.*

3. If you have users who have activated PowerBI via self-service sign-up and have created an unmanaged tenant for your organization, the IT admin can manage this tenant via takeover. [Learn more.](https://powerbi.microsoft.com/documentation/powerbi-admin-administering-power-bi-in-your-organization/#what-is-the-process-to-manage-a-tenant-created-by-Microsoft-for-my-users)

### Recommended documents

[Add a custom domain name in Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain)

[Federated and managed domain names](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#federated-and-managed-domain-names)

## I am unable to delete my domain name

### Recommended steps

1. Ensure that you have removed all users, groups and applications utilizing the domain name you are trying to remove. There cannot be any dependencies on the domain name unless the deletion will fail. [Learn more.](https://support.microsoft.com/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365)

2. If you have multiple sub-domains on your tenant, you will need to remove each before you can delete the root domain. For example, if you have **na.contoso.com** and **emea.contoso.com**, you will need to
delete the child domains before you can delete the parent domain **contoso.com** [Learn more.](https://support.microsoft.com/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365)

### Recommended documents

[Add a custom domain name in Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-add-domain)

[PowerShell for deleting a domain](https://docs.microsoft.com/en-us/powershell/msonline/v1/remove-msoldomain)

## I want to delete the initial .onmicrosoft.com domain

### Recommended steps

1. To delete the existing .onmicrosoft.com domain in turn means deleting the directory instance you have created, this requires you to remove all, users, groups and applications, and cancel your Azure and or Office 365 subscriptions in order to delete the directory. [Learn more.](https://support.microsoft.com/en-us/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365)

2. If you have mistakenly created an Azure AD with an initial .onmicrosoft.com domain such as **myname.onmicrosoft.com** and wish to update it to a friendlier company name like **contoso.onmicrosoft.com** you can configure a new Azure AD and associate your subscriptions with
the target tenant. [Learn more.](https://support.microsoft.com/en-us/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365)*.*

### Recommended documents

[Initial and custom domain names](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-add-domain-concepts#initial-and-custom-domain-names)

[Domain names in Azure AD and other Microsoft Online Services](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-add-domain-concepts#domain-names-in-azure-ad-and-other-microsoft-online-services)
