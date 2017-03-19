<properties
	pageTitle="I want to delete the initial .onmicrosoft.com domain"
	description="Azure Active Directory domains troublehooter"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="curtand"
	displayOrder="4923"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="directory_domain"
	productPesIds=""
	cloudEnvironments="public"
/>

# I want to delete the initial .onmicrosoft.com domain

## Recommended steps

1. To delete the existing .onmicrosoft.com domain in turn means deleting the directory instance you have created, this requires you to remove all, users, groups and applications, and cancel your Azure and or Office 365 subscriptions in order to delete the directory. [Learn more.](https://support.microsoft.com/help/2787210/-unable-to-remove-this-domain-error-when-you-try-to-remove-a-domain-from-office-365)

2. If you have mistakenly created an Azure AD with an initial .onmicrosoft.com domain such as **myname.onmicrosoft.com** and wish to update it to a friendlier company name like **contoso.onmicrosoft.com**, you can configure a new Azure AD and associate your subscriptions with
the target tenant. [Learn more.](https://support.microsoft.com/help/2787792/-domain-has-associated-subdomains-or-you-cannot-remove-a-domain-that-has-subdomains-error-when-you-try-to-remove-a-domain-from-office-365)

## Recommended documents

[Initial and custom domain names](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#initial-and-custom-domain-names)

[Domain names in Azure AD and other Microsoft Online Services](https://docs.microsoft.com/azure/active-directory/active-directory-add-domain-concepts#domain-names-in-azure-ad-and-other-microsoft-online-services)

