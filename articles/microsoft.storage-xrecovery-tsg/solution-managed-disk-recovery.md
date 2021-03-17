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
	ownershipId="StorageMediaEdge_AccountManagement"
	articleId="a41dace6-6bfd-4a84-9761-35344368bac7"
/>

# Managed Disk Recovery

<!--issueDescription-->


>***THIS INFORMATION IS MS INTERNAL ONLY. DO NOT SHARE WITH CUSTOMERS***



For most recent updates with regards to feature and the process of recovering Managed Disk, please refer to wiki page [Disk Management_TSG_Soft Deleted Recovery](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/361491)

<br>

Soft deletion is a new feature introduced by the disk RP, which saves the blobs of deleted disks for up to 4 days, to ensure recovery is possible. This feature is enabled only on managed disks which have been in production for more than 10 days (***THIS INFORMATION IS MS INTERNAL ONLY. DO NOT SHARE WITH CUSTOMERS.***). <br>
<br>

You will need to check if “**SoftDelete**” is enabled on the  disk which is found in the logs using the kusto query below and email about the incident to cssdiskrec@microsoft.com for recovery. **Also be mindful that this is not supported in Ultra Disk.**<br>
<br>

If no “**SoftDelete**” event is present, the disk wasn’t soft deleted: collect the blob URL and **pseudosubscription** and forward the incident to **XStore/Table Server** for recovery. <br> 

<br>
Again If you don’t have direct access to route the ICM to this team,  ask your respective TA to route the ICM or send an email to cssstorageta@microsoft.com.<br>
<br>

> Those steps should be done as quickly as possible, to improve the chances of successful recovery

<br>


Execute: [[Web]](https://dataexplorer.azure.com/clusters/disks.kusto.windows.net/databases/Disks?query=H4sIAAAAAAAEAF2Ry2oCMRSG94W%2bw8GVwqij3arQMqUM2CLarkoZYubopMacNBet0EVfo6%2fXJ2kmSr2sAvkv5ztJJuxqOpmiJW84jsUC%2bY5LvN%2bgctdXX7Ct0CA8khKOjFDLW62l4MwJUjAcQiOL%2bXaIu4qHjGHS2%2bLob0C3C4ODa2BwGYKjE310HGL93HIjdN2dl7H9dfZyl2dv%2b5LZiQ55dpI0B%2fwntkbgpBwTykLDcv%2bxtSVzLO0VWThqjGLsVZHuG6OfFuAqhDJoHcgXsCMPJanf7x8HFdtgVPGTcQfqwp9EMycvS7AroYMgLEihsFPT7eEmBrmw%2bCzWOHNsrWE0hGaAQhdumv20n7bTm3av12rVC2lD7xhGXaaS%2fyUfDHldkydneyegLfqSzl8xgbmk%2bYuRSQSO3%2foHpUkC2vMBAAA%3d)[[Desktop]](https://disks.kusto.windows.net/Disks?query=H4sIAAAAAAAEAF2Ry2oCMRSG94W%2bw8GVwqij3arQMqUM2CLarkoZYubopMacNBet0EVfo6%2fXJ2kmSr2sAvkv5ztJJuxqOpmiJW84jsUC%2bY5LvN%2bgctdXX7Ct0CA8khKOjFDLW62l4MwJUjAcQiOL%2bXaIu4qHjGHS2%2bLob0C3C4ODa2BwGYKjE310HGL93HIjdN2dl7H9dfZyl2dv%2b5LZiQ55dpI0B%2fwntkbgpBwTykLDcv%2bxtSVzLO0VWThqjGLsVZHuG6OfFuAqhDJoHcgXsCMPJanf7x8HFdtgVPGTcQfqwp9EMycvS7AroYMgLEihsFPT7eEmBrmw%2bCzWOHNsrWE0hGaAQhdumv20n7bTm3av12rVC2lD7xhGXaaS%2fyUfDHldkydneyegLfqSzl8xgbmk%2bYuRSQSO3%2foHpUkC2vMBAAA%3d&web=0)[[Web (Lens)]](https://lens.msftcloudes.com/v2/#/discover/query//results?datasource=(cluster:disks.kusto.windows.net,database:Disks,type:Kusto)&query=H4sIAAAAAAAEAF2Ry2oCMRSG94W%2bw8GVwqij3arQMqUM2CLarkoZYubopMacNBet0EVfo6%2fXJ2kmSr2sAvkv5ztJJuxqOpmiJW84jsUC%2bY5LvN%2bgctdXX7Ct0CA8khKOjFDLW62l4MwJUjAcQiOL%2bXaIu4qHjGHS2%2bLob0C3C4ODa2BwGYKjE310HGL93HIjdN2dl7H9dfZyl2dv%2b5LZiQ55dpI0B%2fwntkbgpBwTykLDcv%2bxtSVzLO0VWThqjGLsVZHuG6OfFuAqhDJoHcgXsCMPJanf7x8HFdtgVPGTcQfqwp9EMycvS7AroYMgLEihsFPT7eEmBrmw%2bCzWOHNsrWE0hGaAQhdumv20n7bTm3av12rVC2lD7xhGXaaS%2fyUfDHldkydneyegLfqSzl8xgbmk%2bYuRSQSO3%2foHpUkC2vMBAAA%3d&runquery=1)[[Desktop (SAW)]](https://disks.kusto.windows.net/Disks?query=H4sIAAAAAAAEAF2Ry2oCMRSG94W%2bw8GVwqij3arQMqUM2CLarkoZYubopMacNBet0EVfo6%2fXJ2kmSr2sAvkv5ztJJuxqOpmiJW84jsUC%2bY5LvN%2bgctdXX7Ct0CA8khKOjFDLW62l4MwJUjAcQiOL%2bXaIu4qHjGHS2%2bLob0C3C4ODa2BwGYKjE310HGL93HIjdN2dl7H9dfZyl2dv%2b5LZiQ55dpI0B%2fwntkbgpBwTykLDcv%2bxtSVzLO0VWThqjGLsVZHuG6OfFuAqhDJoHcgXsCMPJanf7x8HFdtgVPGTcQfqwp9EMycvS7AroYMgLEihsFPT7eEmBrmw%2bCzWOHNsrWE0hGaAQhdumv20n7bTm3av12rVC2lD7xhGXaaS%2fyUfDHldkydneyegLfqSzl8xgbmk%2bYuRSQSO3%2foHpUkC2vMBAAA%3d&saw=1) [https://disks.kusto.windows.net/Disks](https://disks.kusto.windows.net/Disks)
```
DiskRPResourceLifecycleEvent
| where MonitoringApplication == "DiskRP-southcentralus_Monitoring" // <DiskRP-<region>_Monitoring>
| where subscriptionId == "45567ff6-8d94-45e1-b9d8-76e1771ccd53" // <Subscription ID>
| where resourceName contains "scuqwsdata01_DataDisk_Lun_0" // <Name of the disk. If you don’t have the exact name of the disk, you could skip this line.>
|where PreciseTimeStamp >= (datetime(2020-03-11))
| project PreciseTimeStamp, resourceGroupName, resourceName, pseudosubscriptionId, blobUrl, diskEvent
```
<br>

1 "PreciseTimeStamp": 2020-07-09T15:07:58.9912377Z <br>
2 "resourceGroupName": CENTRALRG <br>
3 "resourceName": ASVM1_OsDisk1_a456be31d53e438080e281655d50bf81 <br>
4 "presudosubscriptionId": 4653363e-724e-44d0-b583-ebbeaf2a05cd <br>
5 "blobUrl": https://md-c5l4xdhjqzqr.blob.core.windows.net/xt05lzzmn244/abcd <br>
6 "diskEvent": SoftDelete <br>
<br>

## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Managed Disks Recovery](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/361491/Managed-Disks-Recovery)
3. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
4. [Sev 2 IcM to WASU for Managed Disk or Blob Recovery](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=v154BG)
5. [Sev 3 IcM to XStore PG for Managed Disk or Blob Recovery](https://aka.ms/IcMXTableServer)