<properties
	pageTitle="How to check for deletion details from ASC"
	description="How to check for deletion details from ASC"
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
	articleId="deaa5095-2c36-4dc2-bfc1-1fadcc47a67c"
/>

# How to check for deletion details from ASC

1. Navigate to **Resource Explorer** and search for the affected Storage Account resource.
2. Select **Blob** tab/section from the Storage Account information.
3. Navigate to the subsection **Blob/Container Deletion Lookup & Recovery** and input the **Container Name** to attempt recovery.
4. Click + **Get Deletion & Recovery Info** and fill the details of the deletion operation of the resource we are attempting to recover and **Run** the query.
5. Once status is **Succeeded**, review the Result and Recover Status

<br>
<br>

## How to check for deleted container name
<br>
KUSTO

Execute: [Web](https://dataexplorer.azure.com/clusters/armprod.kusto.windows.net/databases/ARMProd?query=H4sIAAAAAAAEAHWQUUvDMBSF3wv9D6Ev7aAIgm8yIXZBCq4dbfYke0iTi6ukSblJ0YE%2f3qwbOpm%2bXc459%2bPcq8ETN3WlIkuSvLTbx3K1S%2b5JHOlgtNSIAcgyGLxu6BOjRVFvK17RNQupOJJ6ch4wSwUOI1qVLm6U8KITDrKUNuvNSWv3Fjr7wYzHHlyAf5L3PSCQDYLsHfB%2bgNaLYSQPRLza7PZOLS5SCM5OKCGUlNZ40Rt37iyM%2btM9F%2f9B2BFQ%2bN6a6qh%2f55IVe2acJTPov0xRV5yWFWuSIy%2bc%2bQbSX1XPwwYi6JlQqvw3Lr%2boOc%2bT9vwwBl0KrQHLkSoV5NNzLCpA0h2u%2fyOcDIk4%2bgK5AtWStwEAAA%3d%3d) [Desktop](https://armprod.kusto.windows.net/ARMProd?query=H4sIAAAAAAAEAHWQUUvDMBSF3wv9D6Ev7aAIgm8yIXZBCq4dbfYke0iTi6ukSblJ0YE%2f3qwbOpm%2bXc459%2bPcq8ETN3WlIkuSvLTbx3K1S%2b5JHOlgtNSIAcgyGLxu6BOjRVFvK17RNQupOJJ6ch4wSwUOI1qVLm6U8KITDrKUNuvNSWv3Fjr7wYzHHlyAf5L3PSCQDYLsHfB%2bgNaLYSQPRLza7PZOLS5SCM5OKCGUlNZ40Rt37iyM%2btM9F%2f9B2BFQ%2bN6a6qh%2f55IVe2acJTPov0xRV5yWFWuSIy%2bc%2bQbSX1XPwwYi6JlQqvw3Lr%2boOc%2bT9vwwBl0KrQHLkSoV5NNzLCpA0h2u%2fyOcDIk4%2bgK5AtWStwEAAA%3d%3d&web=0) [Web (Lens)](https://lens.msftcloudes.com/v2/#/discover/query//results?datasource=(cluster:armprod.kusto.windows.net,database:ARMProd,type:Kusto)&query=H4sIAAAAAAAEAHWQUUvDMBSF3wv9D6Ev7aAIgm8yIXZBCq4dbfYke0iTi6ukSblJ0YE%2f3qwbOpm%2bXc459%2bPcq8ETN3WlIkuSvLTbx3K1S%2b5JHOlgtNSIAcgyGLxu6BOjRVFvK17RNQupOJJ6ch4wSwUOI1qVLm6U8KITDrKUNuvNSWv3Fjr7wYzHHlyAf5L3PSCQDYLsHfB%2bgNaLYSQPRLza7PZOLS5SCM5OKCGUlNZ40Rt37iyM%2btM9F%2f9B2BFQ%2bN6a6qh%2f55IVe2acJTPov0xRV5yWFWuSIy%2bc%2bQbSX1XPwwYi6JlQqvw3Lr%2boOc%2bT9vwwBl0KrQHLkSoV5NNzLCpA0h2u%2fyOcDIk4%2bgK5AtWStwEAAA%3d%3d&runquery=1) [Desktop (SAW)](https://armprod.kusto.windows.net/ARMProd?query=H4sIAAAAAAAEAHWQUUvDMBSF3wv9D6Ev7aAIgm8yIXZBCq4dbfYke0iTi6ukSblJ0YE%2f3qwbOpm%2bXc459%2bPcq8ETN3WlIkuSvLTbx3K1S%2b5JHOlgtNSIAcgyGLxu6BOjRVFvK17RNQupOJJ6ch4wSwUOI1qVLm6U8KITDrKUNuvNSWv3Fjr7wYzHHlyAf5L3PSCQDYLsHfB%2bgNaLYSQPRLza7PZOLS5SCM5OKCGUlNZ40Rt37iyM%2btM9F%2f9B2BFQ%2bN6a6qh%2f55IVe2acJTPov0xRV5yWFWuSIy%2bc%2bQbSX1XPwwYi6JlQqvw3Lr%2boOc%2bT9vwwBl0KrQHLkSoV5NNzLCpA0h2u%2fyOcDIk4%2bgK5AtWStwEAAA%3d%3d&saw=1) [https://armprod.kusto.windows.net/ARMProd)
```kusto
let subId = "[SUBID]"; 
let SAname ="[STORAGEACCOUNTNAME]";
cluster('armprod').database('ARMProd').ShoeboxEntries 
| where PreciseTimeStamp > ago(14d) 
| where resourceId contains subId and resourceId contains SAname 
| where operationName contains "DELETE" and operationName contains "CONTAINER"
| project PreciseTimeStamp, correlationId, operationName, resourceId, resultType, callerIpAddress 
| order by PreciseTimeStamp asc 
```
<br>

Jarvis - [Sample JARVIS Query](https://jarvis-west.dc.ad.msft.net/48E114C0)


```Jarvis
Endpoint: Diagnostics PROD (for public Azure)
Namespace: Xstore
Events to search: DiagnosticAuditLog
Time range: MM/DD/YYYY
Scoping conditions: Tenant == [Stamp Name]
```
```
Filtering conditions
OwnerAccountName contains [STORAGE ACCOUNT NAME]
operationName == DeleteContainer
```
(you can use nslookup .blob.core.windows.net to determine tenant)