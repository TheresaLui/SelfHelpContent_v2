<properties
	pageTitle="Account stuck in created state"
	description="Account stuck in created state"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="bedd0778-5302-4b5f-b04c-00b4989db7e0"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Account stuck in created state

**Azure Support Center(ASC)**

1. Proceed to gather insights of the operation from Azure Support Center (ASC).
2. Navigate to Resource Explorer and select the resource at the Subscription level(top resource).
3. Select Operations tab section.
4. Filter for the suspected timeframe of the operation.
5. Proceed depending of the Deployment Model (Classic/ARM)
    1. **Classic**ː Option 1ː
       1. Look into the ARM Operations subsection.
       2. Filter for Microsoft.ClassicStorage/storageAccounts/write for Creation or Microsoft.ClassicStorage/storageAccounts/delete for Deletion operations. Example(Image).
       3. Review further details on the operation on ASC and/or open the available Kusto / Context Activity / QoS / EG links. Suggestedː HTTP Incoming Kusto Query
    2. **Classic**ː Option 2ː
       1. Look into the RDFE Operations subsection.
       2. Filter for CreateStorageServiceOperation for Creation or DeleteStorageServiceOperation for Deletion operations. Example(Image).
       3. Review further details on the operation on ASC and/or open the available Deployment Context / QoS / EG links.
    3. **ARM**ː
       1. Look into the ARM Operations subsection.
       2. Filter for Microsoft.Storage/storageAccounts/write for CreationMoricrosoft.Storage/storageAccounts/delete for Deletion operations. Example(Image).
       3. Review further details on the operation on ASC and/or open the available Kusto / Context Activity / QoS / EG links. Suggestedː HTTP Incoming Kusto Query
6. Review the details of the query, take note of the CorrelationId and Timestamp and navigate to the next section "Review the details of the recent failed operation" to find more information about the issue.

**Alternatively use Kusto**

   1. Get/Open [Kusto.Explorer](http://kusto/ke/Kusto.Explorer.application) . More information at [Tools reference](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2fGeneralPages%2fAzure%2fAzure_Virtual%20Machine_Tools%20reference).
   2. Open a New Query Tab and Select the Armprod>ARMProd Connection.
   3. Fill the following example queries with your environment details to get further information. ShoeboxEntries Kusto Query:

~~~kusto 

ShoeboxEntries | where resourceId endswith "/<StorageAccountName>" and operationName !contains "LISTKEYS"   
| where PreciseTimeStamp >= datetime("10/11/2018 00:00") and PreciseTimeStamp <= datetime("10/11/2018 23:00:00")    
| project PreciseTimeStamp , resourceId , operationName , resultSignature , properties, correlationId, callerIpAddress, ['identity']

~~~

   4. Review the details of the query, take note of the CorrelationId and Timestamp and navigate to the next section "Review the details of the recent failed operation" to find more information about the issue.

**Review the details of the recent failed operation**

1. Using [Jarvis/MDM](https://jarvis-west.dc.ad.msft.net/logs)
Open Jarvis Logs/MDM and complete the query with the below details. [Query Example](https://jarvis-west.dc.ad.msft.net/F5E7D3D5)

~~~jarvis

MigrationWikiCodeBeginMark
Endpoint: Diagnostics PROD
Namespace: RegionalSRP
Events: ServiceOperationActivityEvent
Region:  <AzureRegion>
Time range:<Timestamp>
Filtering: AnyField contains <CorrelationId>

~~~

3.Within the query results start searching for the conflicting lock operation. Some examples below: Tip: You may filter the search for TraceLevel below or equal than 4 to reduce the relevant logs.

~~~log

Unable to acquire Exclusive Account lock 'StorageAccountName'. Conflicting locks: bc62d9dd-26f7-4dac-a251-88956e7aec08[2018-02-17T13:48:34.3425349Z]

~~~

**Review the details of the operation with the exclusive lock using Jarvis/MDM**

1. Use the same query in the previous section but now use the **OperationId** and **Timestamp** of the locking operation found earlier.
2. Within the query results start searching for the failure reason of the locking operation. Some examples below: Tip: You may filter the search for TraceLevel below or equal than 4 to reduce the relevant logs.

~~~logs

Account creation failed for account StorageAccountName on stamp cq2prdstr03a with Error AccountBeingDeleted, Message: The specified account is in the process of being deleted but still physically exists.
RequestId:eaef4dfe-0004-0004-4505-a15342000000
Time:2018-02-08T17:50:21.5667766Z

~~~

3. Once the error/cause of the issue found:
   1. If the error is related to **AccountBeingDeleted**, this may indicate that a Storage Account with the same name was recently deleted, therefore the inner data of the same has not been fully Garbage Collected(GC). The GC process can take up to 14 days. Therefore some options for the customer:
      1. Create a Storage Account with a different name.
      2. Wait up to 14 days until all the previous Storage Account's data is completely GC'ed.
   2. If the error message implies a trivial resolution or it's actionable, please guide the customer to mitigate the issue based on the error message.
