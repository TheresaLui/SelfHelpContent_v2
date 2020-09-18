<properties
	pageTitle="I tried to create a conditional access policy that blocks all mail apps on my organization's Windows computers. Currently, however, only native mail apps are being blocked."
	description="I tried to create a conditional access policy that blocks all mail apps on my organization's Windows computers. Currently, however, only native mail apps are being blocked. "
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="conditional_access_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ca5cfd6c-817c-4bc8-a2ec-caaafe663bf1"
	ownershipId="IntuneCxP_Intune"
/>

# I tried to create a conditional access policy that blocks all mail apps on my organization's Windows computers. Currently, however, only native mail apps are being blocked. 

## **Recommended steps**

On a Windows computer, conditional access only applies to:

  * The native mail app 
  * Microsoft Office 2016
  * Microsoft Office 2013 when modern authentication is enabled

To block Microsoft Office 2013 when modern authentication is disabled, an earlier version of Office, or to block all mail apps, you must:

  * Register the device in Azure Active Directory.
  * Configure Azure Active Directory Federation Services (ADFS). To learn how to configure ADFS, see [Set up SharePoint Online and Exchange Online for Azure Active Directory conditional access.](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-no-modern-authentication)
