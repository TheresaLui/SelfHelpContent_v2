<properties
	pageTitle="How to check if the recovered classic storage account can be registered in RDFE"
	description="How to check if the recovered classic storage account can be registered in RDFE"
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
	articleId="a716864b-2b05-4e88-a1ad-6038a17941f6"
/>

# How to check if the recovered classic storage account can be registered in RDFE

1. Navigate to Geneva Actions (Jarvis Actions) :  [AzureRT > Storage Management > Register Storage Account](https://jarvis-west.dc.ad.msft.net/441320A3?genevatraceguid=e0246c8a-207b-4120-857b-1be9dc2b2d25)
2. Fill in the requested information as obtained from Account Summary (XLS)
3. Subscription: **Subscription ID**
4. Name of Storage Service: **Storage Account Name**
5. StorageGeoId for storage account: **Geo Domain from XLS**
6. Label for storage account: **Storage Account Name**
7. Location for the service: **Geo Location**
8. Approver:**,**
9. Approver Link: **ICM#**
10. Click on **Get Access** after providing all information.
11. You should now see the JIT Access window. Provide all details as below and click Submit.
12. Work-Item Source: **IcM**
13. Work-Item Id: **IcM ID created in Step 2**
14. Resource Type: **ACIS**
15. Scope: **Storage**
16. Access Level: **PlatformServiceOperator**
17. Click on **Get Access** after providing all information.
18. Once your permissions are approved, you will be reauthenticated. Expect a lot of authentication popups.
19. Once successful, the **Get Access**, and **Refresh Permissions** buttons will be replaced by a "Run" button. Click on that.
20. A successful execution result will return a message like "Successfully registered the storage account"
