<properties
	pageTitle="Managed Disk Recovery"
	description="Managed Disk Recovery"
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
	articleId="a41dace6-6bfd-4a84-9761-35344368bac7"
/>

# Managed Disk Recovery

<!--issueDescription-->
**File an IcM to check for recovery options**

Please explain to customer that recovery is a best effort attempt and is not always guaranteed to be successful. We rely on our customers to follow best practices to safeguard their data.<br>
1. Previosuly in the Properties section, we checked the Type and ensure and it is one of the following eligible<br>
2. Collect business impact to to show that data to recover is production data (not test data).<br>
3. If no backups or copies are available, determine time of deletion and path of blob using the following Kusto query.<br>

~~~kusto 

cluster("disks.kusto.windows.net").database("Disks").DiskRPResourceLifecycleEvent
| where PreciseTimeStamp > ago(2d)
| where subscriptionId == ""
| where diskEvent contains "Delete" and stage == "After"
| project PreciseTimeStamp, MonitoringApplication, resourceGroupName, resourceName, blobUrl, diskType

~~~

4. Choose an ICM Template based on severity and include all deletion information gathered in previous steps<br>
<br><br>
**Important**<br>
<br>
Must mail (xsupportpm@microsoft.com) with detailed business justification and CC (cssstorageta@microsoft.com) and all details of the IcM so we can track such customer requests.

<!--/issueDescription-->

## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
3. [Sev 2 IcM to WASU for Managed Disk or Blob Recovery](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=v154BG)
4. [Sev 3 IcM to XStore PG for Managed Disk or Blob Recovery](https://aka.ms/IcMXTableServer)