<properties
	pageTitle="How to check the storage content type"
	description="How to check the storage content type"
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
	articleId="b940699d-609f-41d6-bf24-012c0e7ef4b1"
/>

# How to check the storage content type


Use this TSG for a request to recover storage data. As you follow the steps in this TSG, keep notes of each command run and output generated. If you run into any difficulties, this information will be critical to determine your next steps.

**Notes:**

1. Recovery is only possible for certain types of resources, and even then, only if the data has not been garbage collected.
2. Recovery is possible if customer re-creates a Storage Account with the same name. However, it is not possible with any other resource types because the data will be overwritten.
3. It can generally take anywhere from "immediately after deletion" to 14 days for the Storage service to perform garbage collection, so there is no SLA or guarantee of recovery.
4. Set customer expectations in your initial response itself that Azure Support will try recovery on a best-effort basis, but cannot guarantee recovery.
5. Check if the customer created a new resource with the same name (even briefly). Creating a resource with the same name reduces the chances of recovery considerably because it can trigger early cleanup.


