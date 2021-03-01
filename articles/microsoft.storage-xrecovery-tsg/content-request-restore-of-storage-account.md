<properties
	pageTitle="How to request restore of storage account"
	description="How to request restore of storage account"
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
	articleId="b7c745a0-79aa-409d-bd24-7ece31fb4442"
/>

# How to request restore of storage account

**Note:** If you are not a member of TM-CSSStgRec, you won't be able to recover the storage account. Follow these steps:
-  Create an [ICM](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=74a1g3). Be sure to use that link and **not** the ASC method.
- Send an email with the ICM to cssstgrec@microsoft.com to help the Restore Storage Account operation. Provide the ICM number in the email to the recovery team. 
- For ARR customers, send an email to arrstgrecovery@microsoft.com

If you are a member of TM-CSSStgRec, perform the following steps:

1. Go to [JIT ICM Template ](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=74a1g3), Be sure to use this link and **not** the ASC method.
2. Navigate to Geneva Actions (Jarvis Actions) through [SRP > SRP Operations > Restore Storage Account](https://jarvis-west.dc.ad.msft.net/4E6B1757?genevatraceguid=d42c3a17-2955-489e-abfc-d4610df8017c)
3. Request JIT elevation for **Storage-PlatformServiceOperator** . Click **GET ACCESS** from the same blade.
4. Fill in the requested information and click **Run**.
   - Subscription, Storage Account, Region are the same as in Step 1.
   - Creation time is cut and pasted from the creation time in Step 1 (2016-10-12T09:28:08.4824822Z in the example).
   - Stamp name can be left blank.
5. Possible failures at this step are:
  - Account name already in use : This may be because the account was re-created by the customer. Depending on the situation, this may make the original account unrecoverable. The customer should delete the new version of the account, and this TSG should be re-run from the beginning.
  - Account not found : This may be because the account was re-created by the customer, and it did indeed make the original account unrecoverable.
6. Successful completion will look like the following:

>Messages   **Result**  Preview
Restore Storage Account

1 {}
