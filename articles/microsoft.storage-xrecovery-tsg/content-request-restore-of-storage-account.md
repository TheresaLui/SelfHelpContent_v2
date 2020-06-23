<properties
	pageTitle="How to request restore of storage account"
	description="How to request restore of storage account"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="b7c745a0-79aa-409d-bd24-7ece31fb4442"
/>

# How to request restore of storage account

1. Navigate to Geneva Actions (Jarvis Actions) :[SRP > SRP Operations > Restore Storage Account](https://jarvis-west.dc.ad.msft.net/4E6B1757?genevatraceguid=d42c3a17-2955-489e-abfc-d4610df8017c)
2. Request JIT elevation for Storage-PlatformServiceOperator (and NOT PlatformServiceAdministrator), you can click GET ACCESS from the same blade.
3. Fill in the requested information and hit "Run".
    1. Subscription, Storage Account, Region are the same as in Step 1.
    2. Creation time is cut and paste from the creation time found in Step 1 (2016-10-12T09:28:08.4824822Z in the example).
	3. Stamp name can be left blank.
4. Possible failures at this step are:
	1. Account name already in use : This may be because the account was re-created by the customer. Depending on the situation, this may make the original account unrecoverable. The customer should delete the new version of the account, and this TSG should be re-run from the beginning.
	2. Account not found : This may be because the account was re-created by the customer, and it did indeed make the original account unrecoverable.
5. Successful completion will look like the following "{}"
