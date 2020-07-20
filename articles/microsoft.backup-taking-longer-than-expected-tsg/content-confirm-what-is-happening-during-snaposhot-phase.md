<properties
	pageTitle="Confirm what is happening during snapshot phase "
	description="Confirm what is happening during snapshot phase "
	service=""
	resource=""
	authors="TestAuthor"
	ms.author="TestAuthor"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7fb9c253-70a6-49c3-8238-2cced4081a22"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Confirm what is happening during snapshot phase 

1. Confirm if we are failing and retriying the Snapshot operation
2. Use the following query to get the OperationId from CRP table for the snapshot operation:

~~~kusto

Execute: [Web] [Desktop] [Web (Lens)] [Desktop (SAW)] https://azcrp.kusto.windows.net/crp_allprod 
database("crp_allprod").ApiQosEvent
| where PreciseTimeStamp >=  datetime(2019-11-25 14:33:46.9036479)  and PreciseTimeStamp < datetime(2019-11-26 18:36:12.7320144) // replace date and time with start and end time of backup operation 
| where clientApplicationId == "Backup Management Service"
| where subscriptionId ==  "<subscriptionId>"
| where operationName contains "RestorePoints.RestorePointOperation.PUT"
| where resourceName contains "<vm-name>" // replace with the VMname
| project PreciseTimeStamp, durationIn
Milliseconds, e2EDurationInMilliseconds,  operationName , resourceGroupName, resourceName, httpStatusCode, resultCode, errorDetails, clientApplicationId, subsc

~~~

3. Confirm if you see restorepoint.put operation  several times and with failure.  
4. Please engage your TA to review the extension logs and the context of the operation to decide if the reason of the snapshot failing and retry taking longer require other teams collaboration or PG 

## Recommended Documents

1. https://supportability.visualstudio.com/AzureBackup/_wiki/wikis/AzureBackup/184551/Azure-VM-Backup-Performance?anchor=snapshot-phase-of-the-backup-takes-a-long-time
