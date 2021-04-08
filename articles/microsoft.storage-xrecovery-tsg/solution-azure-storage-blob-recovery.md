<properties
	pageTitle="Azure Storage Blob Recovery"
	description="Azure Storage Blob Recovery"
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
	articleId="e542e56b-e181-411d-8f2a-8f163314f035"
/>

# Azure Storage Blob Recovery

<!--issueDescription-->
1. Previosuly in the Properties section, we checked the Type and ensure and it is one of the following eligible<br>
	1. Standard_GRS<br>
	2. Standard_RAGRS<br>
	3. Standard_GZRS<br>
	4. Standard_RAGZRS<br>
2. Collect business impact to to show that data to recover is production data (not test data).<br>
3. Confirm that a new blob with the same name has NOT created. If so all data would be cleaned up and is lost.<br>
4. Navigate to the storage resource in Azure Support Center Resource Explorer.<br>
5. Click on the Blob tab and choose Search Blob/Container.<br>
6. Choose "Blob" to lookup a blob and provide the blob path as container/full_path_of_blob.<br>
7. Click Run<br>
8. If the blob entry is found ensure the deletion date agrees with either of the following conditions to see if we can proceed with recovery IcM.<br>
9. Less than a week for Standard Storage<br>
10. Less than 3 days for Premium Storage<br>
11. Choose an ICM Template based on severity and include all deletion information gathered in previous steps<br>

<!--/issueDescription-->

## Recommended Documents

1. [Sev 3 IcM to XStore PG for Managed Disk or Blob Recovery](https://aka.ms/IcMXTableServer)
