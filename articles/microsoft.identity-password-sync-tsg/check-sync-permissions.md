<properties
	pageTitle="Check connect user permissions"
	description="check connect user permissions"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8e331ffc-3195-4060-9286-a22c1d69a248"
/>

# How to check connect user permissions

* A powershell command exists to set permissions
* There is no command to test or check permissions
* The powershell command is as follows

~~~powershell

Set-ADSyncPasswordHashSyncPermissions -ADConnectorAccountName <String> -ADConnectorAccountDomain <String>

~~~


## **Recommended Documents**

* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Azure AD Connect: Configure AD DS Connector Account Permissions](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account)
