<properties
	pageTitle="I have configured federation with Azure AD using AD FS but sign-in is failing"
	description="Sign in is failing with Azure AD federation"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="billmath"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32570971"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I have configured federation with Azure AD using AD FS but sign-in is failing

## Recommended Steps

It is recommended to use Azure AD Connect to configure federation with Azure Active Directory. Azure AD Connect provides easy steps to configure and maintain federation. If user sign-in is failing, see if the below common resolution can help – 


1. [Repair trust with Azure AD using AAD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#repairthetrust)
2. [Configure federation with multiple domains](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#addfeddomain)
3. [Configure federation with alternate ID](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-federation-management#federate-with-azure-ad-using-alternateid)
4. [Configure WIA for users in browsers other than Internet Explorer](https://technet.microsoft.com/windows-server-docs/identity/ad-fs/operations/configure-intranet-forms-based-authentication-for-devices-that-do-not-support-wia)
