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
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check connect user permissions

1. A powershell command exists to set permissions
2. There is no command to test or check permissions
3. The powershell command is as follows

~~~powershell

Set-ADSyncPasswordHashSyncPermissions -ADConnectorAccountName <String> -ADConnectorAccountDomain <String>

~~~


## Recommended Documents

1. [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/reference-connect-accounts-permissions)
2. [Azure AD Connect: Configure AD DS Connector Account Permissions](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account)
