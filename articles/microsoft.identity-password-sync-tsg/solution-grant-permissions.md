<properties
	pageTitle="Grant permissions"
	description="Grant permissions"
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
	articleId="2350d2f1-d897-4527-a962-0e4818712c6e"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Grant permissions

<!--issueDescription-->

1. A powershell command exists to set permissions
2. There is no command to test or check permissions
3. The powershell command is as follows

~~~powershell

Set-ADSyncPasswordHashSyncPermissions -ADConnectorAccountName <String> -ADConnectorAccountDomain <String>

~~~

<!--/issueDescription-->

## Recommended Documents

1. [Azure AD Connect: Configure AD DS Connector Account Permissions](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account)
