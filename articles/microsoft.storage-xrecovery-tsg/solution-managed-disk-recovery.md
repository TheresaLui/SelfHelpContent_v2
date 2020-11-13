<properties
	pageTitle="Managed Disk Recovery"
	description="Managed Disk Recovery"
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
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="a41dace6-6bfd-4a84-9761-35344368bac7"
/>

# Managed Disk Recovery

<!--issueDescription-->


## Recover a Soft Deleted Managed Disk
<br>


>***THIS INFORMATION IS MS INTERNAL ONLY. DO NOT SHARE WITH CUSTOMERS***

<br>

**Engineer Prequisites to Recover a Soft Deleted Disk**

Members of the Managed Disk Recovery Team (Managed Disk SMEs, Storage SMEs, Global IaaS VM TAs) will need to log into their SAW/SAVM with Azure Management Environment (AME) credentials.

<br>

 [AME Account Creation and Smartcard Request](https://microsoft.sharepoint.com/teams/AME/SitePages/AME%20Account%20and%20Smartcard%20Request.aspx)

[Prerequisites to Use Your SAW with AME](https://strikecommunity.azurewebsites.net/articles/6709/prerequisites-to-use-your-saw-with-ame.html)

[Using SAVM](https://strikecommunity.azurewebsites.net/articles/4282/using-savm.html)

<br>

**SUMMARY**

We can now recover managed disks that have been deleted if they are in a soft deleted state. A managed disk will be in a soft deleted state if:

1. The disk was created more than 10 days prior to the deletion.<br>
2. The disk was deleted less than 4 days (96 hours) ago.<br>
3. Ultra Disk is not supported for Soft Delete Recovery.<br>
<br>
>**If a disk cannot be recovered using soft delete recovery,** [follow the process for Azure Incident Management to perform the recovery.](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account?anchor=**disk%2Fblob-recovery**) By opening a [Sev 2/3 IcM](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=e3t1bN)  to Azure Incident Management.

<br>**Overview of the Recovery process**<br>
1. Customer deletes a Managed Disk.<br>
2. Customer opens a service request to restore the Managed Disk.<br>
3. Support Engineer gathers the disk's details, and validates it can be restored.<br>
4. Support Engineer opens an IcM, and e-mails the Managed Disk Recovery Team.<br>
5. Recovery Team member acknowledges the IcM, and uses it to submit a JIT request.<br>
6. Recovery Team member submits the restore request through Jarvis Actions.<br>
7. Recovery Team member notifies the Support Engineer that the restore request has been processed.<br>
<br>

**ASC**<br>
Locate disk and determine if it can be restored (ASC)

<br>

*Resource Group View*

1. Expand Resource Group<br>

2. Expand Microsoft.Compute<br>
3. Select disks<br>
4. Locate deleted disk with the Disk Event, "Soft Deleted". (***Disks marked "Hard Deleted" cannot be restored using this method.***)
5. Create an IcM to restore the Disk<br>
Request Template: [IcM Template](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=HO3f2P)
6. Send an E-mail to the [Managed Disk Recovery Team](cssdiskrec@microsoft.com) with the details of the IcM and the:
<br> o SR Number<br>
o Subscription Id<br>
o DiskRP Region<br>
o Source RG Name<br>
o Source Disk Name<br>
o Target RG Name<br>
o Target Disk Name<br>
<br>

*Resource Provider View*
1. Expand Microsoft.Compute<br>

2. Select disks<br>
3. Locate deleted disk with the Disk Event, "Soft Deleted". (***Disks marked "Hard Deleted" cannot be restored using this method.***)
4. Create an IcM to restore the Disk<br>
Request Template: [IcM Template](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=HO3f2P)
5. Send an E-mail to the [Managed Disk Recovery Team](cssdiskrec@microsoft.com) with the details of the IcM and the:<br>
o SR Number:<br>
o Subscription Id:<br>
o DiskRP Region:<br>
o Source RG Name:<br>
o Source Disk Name:<br>
o Target RG Name:<br>
o Target Disk Name: <br>
<br>

**KUSTO**

Locate disk and determine if it can be restored (Kusto)
1. Run the following Kusto query:

Execute in [Web](https://dataexplorer.azure.com/clusters/disks/databases/Disks?query=H4sIAAAAAAAAA11SQW7CMBC89xWrnEBKIOXSCyBVTVUhtRUK9Bw5zoa4GG9kO7RIPfQb%2FV5fUtugUDju7uzMztiZMNt8maOhTnN8FjXyA5f4uEdlb77go0GN8EJKWNJCbe7bVgrOrCAFsxlEWVhPuENrJjtTnKERjMewQgu2Qchx41emJ%2Fz0WM%2F%2Fwee9mulKw7VovciiCjKrfy1YZBEcuSXyI%2F3VvKfSJ1%20vbIfASVkmlIHIlwXVReYYLFaFv8qfmyQwDVCqA23l%20iNY1HCgDipSv98%2FFhq2xzDFT%20bk1RU%20DmBOnazAbEXrBsKAFApHZ4tLjVwYXIsdrizbtTCfwaBiFq3rDCbpJE3SuyS9HQ6D04eGyCAw8GMwDWkrD1BiTRp7Yai8GxeAU2k1vftsrnXiPpEnTV3rvcYXIcXQGuwqunyDGEpJ5ZuWcVAKnyOGfLlGxZT9A3NsM7xDAgAA)  [Desktop](https://disks.kusto.windows.net/Disks?query=H4sIAAAAAAAAA11SQW7CMBC89xWrnEBKIOXSCyBVTVUhtRUK9Bw5zoa4GG9kO7RIPfQb%2FV5fUtugUDju7uzMztiZMNt8maOhTnN8FjXyA5f4uEdlb77go0GN8EJKWNJCbe7bVgrOrCAFsxlEWVhPuENrJjtTnKERjMewQgu2Qchx41emJ%2Fz0WM%2F%2Fwee9mulKw7VovciiCjKrfy1YZBEcuSXyI%2F3VvKfSJ1%20vbIfASVkmlIHIlwXVReYYLFaFv8qfmyQwDVCqA23l%20iNY1HCgDipSv98%2FFhq2xzDFT%20bk1RU%20DmBOnazAbEXrBsKAFApHZ4tLjVwYXIsdrizbtTCfwaBiFq3rDCbpJE3SuyS9HQ6D04eGyCAw8GMwDWkrD1BiTRp7Yai8GxeAU2k1vftsrnXiPpEnTV3rvcYXIcXQGuwqunyDGEpJ5ZuWcVAKnyOGfLlGxZT9A3NsM7xDAgAA&web=0)  [cluster('disks.kusto.windows.net').database('Disks')](https://dataexplorer.azure.com/clusters/disks/databases/Disks)

```Kusto query
   DiskRPResourceLifecycleEvent
   | where MonitoringApplication == "DiskRP-centralus_Monitoring" //-- Set the Region <DiskRP-<Region>_Monitoring>
   | where subscriptionId == "Subscription ID" //-- Select the Subscription ID
   | where resourceName contains "Name_of_Deleted_Disk" //-- <Name of the disk. If you don’t have the name of the disk, you could skip this line.>
   | where PreciseTimeStamp >= (datetime(2020-07-01)) //-- Choose a time shortly before the disk deletion
   | project PreciseTimeStamp, resourceGroupName, resourceName, pseudosubscriptionId, blobUrl, diskEvent, RPTenant
```
2. Find the disk and verify the "diskEvent" is SoftDelete

```output
1 "PreciseTimeStamp": 2020-07-09T15:07:58.9912377Z,
2 "resourceGroupName": CENTRALRG,
3 "resourceName": ASVM1_OsDisk1_a456be31d53e438080e281655d50bf81,
4 "presudosubscriptionId": 4653363e-724e-44d0-b583-ebbeaf2a05cd,
5 "blobUrl": https://md-c5l4xdhjqzqr.blob.core.windows.net/xt05lzzmn244/abcd,
6 "diskEvent": SoftDelete,
7 "RPTenant": DiskRP-centralus,
8
```
3. Create an IcM to restore the disk<br>
o Request Template: [IcM Template](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=HO3f2P)

4. Send an E-mail to the [Managed Disk Recovery Team](cssdiskrec@microsoft.com) with the details of the IcM and the:
<br>
o SR Number:<br>
o Subscription Id:<br>
o DiskRP Region:<br>
o Source RG Name:<br>
o Source Disk Name:<br>
o Target RG Name:<br>
o Target Disk Name:<br>
o Results from [Kusto soft delete query](https://dataexplorer.azure.com/clusters/disks/databases/Disks?query=H4sIAAAAAAAAA11SQW7CMBC89xWrnEBKIOXSCyBVTVUhtRUK9Bw5zoa4GG9kO7RIPfQb%2FV5fUtugUDju7uzMztiZMNt8maOhTnN8FjXyA5f4uEdlb77go0GN8EJKWNJCbe7bVgrOrCAFsxlEWVhPuENrJjtTnKERjMewQgu2Qchx41emJ%2Fz0WM%2F%2Fwee9mulKw7VovciiCjKrfy1YZBEcuSXyI%2F3VvKfSJ1%20vbIfASVkmlIHIlwXVReYYLFaFv8qfmyQwDVCqA23l%20iNY1HCgDipSv98%2FFhq2xzDFT%20bk1RU%20DmBOnazAbEXrBsKAFApHZ4tLjVwYXIsdrizbtTCfwaBiFq3rDCbpJE3SuyS9HQ6D04eGyCAw8GMwDWkrD1BiTRp7Yai8GxeAU2k1vftsrnXiPpEnTV3rvcYXIcXQGuwqunyDGEpJ5ZuWcVAKnyOGfLlGxZT9A3NsM7xDAgAA)





## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Managed Disks Recovery](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/361491/Managed-Disks-Recovery)
3. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
4. [Sev 2 IcM to WASU for Managed Disk or Blob Recovery](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=v154BG)
5. [Sev 3 IcM to XStore PG for Managed Disk or Blob Recovery](https://aka.ms/IcMXTableServer)