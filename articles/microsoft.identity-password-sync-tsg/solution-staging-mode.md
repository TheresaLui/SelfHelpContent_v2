<properties
	pageTitle="Password Hash Sync does not work when the AADConnect server is in staging mode"
	description="Password Hash Sync does not work when the AADConnect server is in staging mode"
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
	articleId="377cab24-731b-4dba-b142-6f91f332a826"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Password Hash Sync does not work when the AADConnect server is in staging mode

<!--issueDescription-->

1. When the Azure AD Connect server is in staging mode, no password hashes are synced to Azure AD
2. If you want to sync password hashes with this server you need to take it out of staging mode

<!--/issueDescription-->

## Recommended Documents

You can read more about how to do that in [this article](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sync-staging-server#switch-active-server).
