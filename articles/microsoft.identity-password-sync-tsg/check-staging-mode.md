<properties
	pageTitle="Check if a server is in staging mode"
	description="Check if a server is in staging mode"
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
	articleId="21ed34df-bd3d-431a-b54c-12c691a8932c"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if a server is in staging mode

1. We need to know if this server is in staging mode. To determine if a server is in staging mode, perform the following:
2. Open Azure AD Connect Wizard from the Desktop Icon, click Configure, then Configure Staging Mode
3. Provide the tenant's Global Administrator credentials and click Next
4. Staging mode is enabled if 'Enable Staging Mode' is checked. 
5. This can also be determined in powershell by using the following command

~~~powershell

(Get-ADSyncGlobalSettings).Parameters | Where-Object {$_.Name -like '*StagingMode*'} | Select Name, Value

~~~

## Recommended Documents

1. To read about staging mode, please refer to (https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sync-staging-server#staging-mode).
