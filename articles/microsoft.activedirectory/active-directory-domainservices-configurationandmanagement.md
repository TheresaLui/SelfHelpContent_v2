<properties
	pageTitle="Configuration, Management and Integration issues"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="arluca"
	selfHelpType="generic"
	supportTopicIds="32447390"
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Configuration, Management and Integration issues

## Unable to complete certain administrative tasks

Members of the 'AAD DC Administrators' group are granted the necessary privileges to perform only the following tasks on the managed domain:

1.	Join Machines to the managed domain.
2.	Configure the built-in GPO for the 'AADDC Computers' and 'AADDC Users' containers in the managed domain.
3.	Administer DNS on the managed domain.
4.	Create and administer customer Organizational Units (OUs) on the managed domain.
5.	Gain administrative access to computers joined to the managed domain. 

For more information, please see [administrative privileges you do not have on a managed domain.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)

## Administrator unable to sign in to the Azure AD Domain Services managed domain

1.	Try to sign in using the UPN format (for example, 'joeuser@contoso.com') instead of the SAMAccountName format ('CONTOSO\joeuser').
2.	Ensure that you have [enabled password synchronization](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-getting-started-password-sync) in accordance with the steps outlined in the Getting Started guide.
3.	Ensure the Virtual machine being used is domain-joined to your managed domain. 
4.	Ensure the user account being used, belongs to the 'AAD DC Administrators' group.

## **Recommended documents**
* [Users removed from your Azure AD tenant are not removed from your managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#users-removed-from-your-azure-ad-tenant-are-not-removed-from-your-managed-domain)
* [Administrative privileges you do not have on a managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD Domain Services - Troubleshooting guide](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting)
* [Azure AD Domain Services FAQs](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)
