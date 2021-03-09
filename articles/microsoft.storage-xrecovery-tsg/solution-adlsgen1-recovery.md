<properties
	pageTitle="ADLS Gen 1 Recovery"
	description="ADLS Gen 1 Recovery"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="symondsk"
	ms.author="ksymonds"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
	articleId="6e380f10-e4a8-4247-8c19-c890e4dbedc9"
/>

# ADLS Gen 1 Recovery #

<!--issueDescription-->

1. This is available 'as-is', and there is no guarantee of recovery <br>
2. When this happens, ADLS Gen 1 name, sub and possible the folders/files to be recovered is what should be provided <br>
3. ADLS Gen 1 PG should be contacted as soon as possible after the accidental delete <br>

**In addition for encrypted accounts:**

* We are unable to recover an encrypted account to an alternate account name. If an account with the same name has been created after the delete, recovery will not be possible. <br>

* If the account used a customer managed master encryption key stored in Azure Key Vault, the Key Vault and/or master encryption key must be restored and access given to ADLS Gen 1 before recovery can proceed. If this cannot be done, recover will not be possible.

<!--/issueDescription-->