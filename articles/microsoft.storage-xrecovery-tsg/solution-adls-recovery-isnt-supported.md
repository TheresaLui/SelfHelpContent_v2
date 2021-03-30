<properties
	pageTitle="ADLS Gen 2 Filesystem and data recovery"
	description="ADLS Gen 2 Filesystem and data recovery"
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
	articleId="61814b58-0c40-4aea-902f-d8cd91a3cee3"
/>

# ADLS Gen 2 Filesystem and data recovery

<!--issueDescription-->

1. First confirm this is an ADLS Gen2 storage account by browsing the storage account resource in **ASC | Resource Explorer** then look for the configuration setting **Data Lake Storage Gen2 Hierarchical Namespace Enabled**.  This should be set to **Enabled**.  If it is set to **Disabled** then this is a blob only storage account and the blob recovery TSG should be followed instead. 
</br>

```
NOTE: Blob recovery is supported by the IaaS Storage team so update the SAP and Support Topic and route the support case to them.
```

</br>

2. Ask the customer if the data has been deleted in the past 7 days.  We can only attempt recovery if the data was deleted in the past 7 days and even then recovery is best effort and not guaranteed.  Please set customer expectations that recovery is not guaranteed. 
</br>

```
NOTE: If the data was deleted > 7 days ago inform the customer that recovery is not possible.
```

</br>

3. If the whole storage account needs to be recovered, ask customer to try from Azure portal first by following the steps on this doc:  

[Recover a deleted storage account - Azure Storage | Microsoft Docs](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-recover?toc=/azure/storage/blobs/toc.json)

</br>

4. If the data was deleted in the past 7 days or the customer is not sure when the data was deleted then open an ICM using the Sev-2 ICM template, however change the Owning Team to ```XStore\Big Data.```  Make sure to include the full path to the storage data (Filesystem, Folder or File) that needs to be recovered.  This path should include the filesystem/container name. 

</br>

**Owning Team**</br>
```Xstore/Big Data```

</br> 

Note: **Xstore\Big Data** is private team now so we cannot select this team when we create IcM ticket.  Big Data PG said we should change Owning team "```Xstore\Triage```" first. If you can select ```Xstore\Big Data```, you may get below error when you try to transfer. If you can select Xstore\Big Data, please go ahead to create IcM to this team. 

## Recommended Documents

1. [http://aka.ms/sarecovery](http://aka.ms/sarecovery)

<!--/issueDescription-->