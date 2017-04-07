<properties
	pageTitle="Other questions regarding Azure AD Domain Services"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="arluca"
	selfHelpType="generic"
	supportTopicIds="32565593"
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Troubleshooting common Azure AD Domain Services issues

## Unable to enable Azure AD Domain Services for your Azure AD Directory. 

Click the error message you encounter, for appropriate troubleshooting steps:

*	[The name contoso100.com is already in use on this network. Specify a name that is not in use.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#domain-name-conflict)
*	[Domain Services could not be enabled in this Azure AD tenant. The service does not have adequate permissions to the application called 'Azure AD Domain Services Sync'. Delete the application called 'Azure AD Domain Services Sync' and then try to enable Domain Services for your Azure AD tenant.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#inadequate-permissions)
*	[Domain Services could not be enabled in this Azure AD tenant. The Domain Services application in your Azure AD tenant does not have the required permissions to enable Domain Services. Delete the application with the application identifier d87dcbc6-a371-462e-88e3-28ad15ec4e64 and then try to enable Domain Services for your Azure AD tenant.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#invalid-configuration)
*	[Domain Services could not be enabled in this Azure AD tenant. The Microsoft Azure AD application is disabled in your Azure AD tenant. Enable the application with the application identifier 00000002-0000-0000-c000-000000000000 and then try to enable Domain Services for your Azure AD tenant.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#microsoft-graph-disabled.)

## Users are unable to sign in to the Azure AD Domain Services managed domain

1.	Try to sign in using the UPN format (for example, 'joeuser@contoso.com') instead of the SAMAccountName format ('CONTOSO\joeuser'). 
2.	Ensure that you have [enabled password synchronization](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync) in accordance with the steps outlined in the Getting Started guide.
3.	Note: Ensure that the affected user account is not an external account in the Azure AD tenant. External users cannot sign in to the managed domain, since Azure AD Domain Services does not have credentials for such user accounts.
4.	If the affected user account is a cloud-only user account: Ensure that the user has changed their password after you enabled Azure AD Domain Services. This step causes the credential hashes required for Azure AD Domain Services to be generated.
5.	If the affected user accounts are synchronized from an on-premises directory: Verify that the [recommended release of Azure AD Connect](https://www.microsoft.com/download/details.aspx?id=47594) has been configured to [perform a full synchronization.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync)
6.	If issues persist after confirming step #4, execute the following commands from your sync machine: 1. "net stop 'Microsoft Azure AD Sync'" 2. "net start 'Microsoft Azure AD Sync'"

## **Recommended documents**
* [Users removed from your Azure AD tenant are not removed from your managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#users-removed-from-your-azure-ad-tenant-are-not-removed-from-your-managed-domain)
* [Administrative privileges you do not have on a managed domain](https://docs.microsoft.com/en-us/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD Domain Services FAQs](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)
