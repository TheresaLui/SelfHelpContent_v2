<properties
	pageTitle="ADLS Gen 2 How to check the creation time of storage account"
	description="How to check the creation time of storage account"
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
	articleId="d24074b9-92e2-4115-aa59-b313542f1362"
/>

# ADLS Gen 2 How to check the creation time of storage account

1. Navigate to Geneva Actions: [SRP > SRP Operations > Get Deleted Storage Account](https://jarvis-west.dc.ad.msft.net/271CD959?genevatraceguid=d42c3a17-2955-489e-abfc-d4610df8017c)
2. Fill in the requested information and click **Run**.

Successful completion will look like the following example SA output:

```
{
    "DeletedAccount": {
        "value": [
            {
                "key": "storagekjs|2020-10-07t11:43:32.9192421z",
                "name": "storagekjs",
                "location": "northeurope",
                "subscription": "11111111-1111-1111-1111-111111111111",
                "resourceGroupName": "storage-test",
                "creationTime": "2020-10-07T11:43:32.9192421Z",
                "deletionTime": "2020-10-07T11:57:31.0807017Z",
                "primaryStampName": "db3prdstr11a",
                "geoPrimaryRegion": "europenorth",
                "geoSecondaryRegion": "europewest"
            }
        ]
    }
}
```

**Note:** If you receive the error message "Account not found," this may be because of the following reasons:

* The provided information is incorrect, or
* The deletion time was more than 14 days in the past (in which case the account cannot be recovered), or
* The account was a Microsoft.ClassicStorage account or RDFE account, which should be recovered with by running the classic account recovery ASC troubleshooter or [TSG 1187811](http://vstfrd:8080/Azure/RD/_workitems?id=1187811&_a=edit) instead, or
* There is some issue with the Deleted Accounts list in SRP, in which case you can engage the XStore > Location Service DRI.
