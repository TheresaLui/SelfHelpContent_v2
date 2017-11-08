<properties
	pageTitle="Demo - Unable to enable Azure AD Domain Services for your Azure AD Directory"
	description="Azure AD Domain Services"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="arluca"
	selfHelpType="resource"
	displayOrder="200"
	cloudEnvironments="public"
/>

# Demo - Unable to enable Azure AD Domain Services for your Azure AD Directory

## **Recommended steps**
Click the error message you encounter, for appropriate troubleshooting steps. It is recommended to use Azure AD Connect to configure federation with Azure Active Directory. Azure AD Connect provides easy steps to configure and maintain federation. If user sign-in is failing, see if the below common resolution can help.

*	[The name contoso100.com is already in use on this network. Specify a name that is not in use.](https://docs.microsoft.com/es-es/azure/active-directory-domain-services/active-directory-ds-troubleshooting#domain-name-conflict)
*	[Domain Services could not be enabled in this Azure AD tenant. The service does not have adequate permissions to the application called 'Azure AD Domain Services Sync'. Delete the application called 'Azure AD Domain Services Sync' and then try to enable Domain Services for your Azure AD tenant].(https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#inadequate-permissions)
*	[Domain Services could not be enabled in this Azure AD tenant. The Domain Services application in your Azure AD tenant does not have the required permissions to enable Domain Services. Delete the application with the application identifier d87dcbc6-a371-462e-88e3-28ad15ec4e64 and then try to enable Domain Services for your Azure AD tenant.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#invalid-configuration)
*	[Domain Services could not be enabled in this Azure AD tenant. The Microsoft Azure AD application is disabled in your Azure AD tenant. Enable the application with the application identifier 00000002-0000-0000-c000-000000000000 and then try to enable Domain Services for your Azure AD tenant.](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshooting#microsoft-graph-disabled)

## **Recommended documents**
Please use the following documents.
* [Administrative privileges you do not have on a managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-admin-guide-administer-domain#administrative-privileges-you-do-not-have-on-a-managed-domain)
* [Azure AD Domain Services FAQs](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-faqs)
* [Automatic Device Registration](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-automatic-device-registration-troubleshoot-windows)