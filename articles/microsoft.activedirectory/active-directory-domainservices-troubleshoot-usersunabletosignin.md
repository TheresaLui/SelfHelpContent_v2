<properties
	pageTitle="Users are unable to sign in to the Azure AD Domain Services managed domain "
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="arluca"
	selfHelpType="resource"
	displayOrder="200"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="8de5601a-c38c-49a0-b4fc-5e5ddde86f41"
	ownershipId="AzureIdentity_DomainName"
/>

# Users are unable to sign in to the Azure AD Domain Services managed domain

## **Recommended steps**
1.	Try to sign in using the UPN format (for example, 'joeuser@contoso.com') instead of the SAMAccountName format ('CONTOSO\joeuser'). 
2.	Ensure that you have [enabled password synchronization](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync) in accordance with the steps outlined in the Getting Started guide.
3.	Note: Ensure that the affected user account is not an external account in the Azure AD tenant. External users cannot sign in to the managed domain, since Azure AD Domain Services does not have credentials for such user accounts.
4.	If the affected user account is a cloud-only user account: Ensure that the user has changed their password after you enabled Azure AD Domain Services. This step causes the credential hashes required for Azure AD Domain Services to be generated.
5.	If the affected user accounts are synchronized from an on-premises directory: Verify that the [recommended release of Azure AD Connect](https://www.microsoft.com/download/details.aspx?id=47594) has been configured to [perform a full synchronization.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync)
6.	If issues persist after confirming step #4, execute the following commands from your sync machine: 1. "net stop 'Microsoft Azure AD Sync'" 2. "net start 'Microsoft Azure AD Sync'"

## **Recommended documents**
* [Administrative privileges you do not have on a managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD Domain Services FAQs](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)
