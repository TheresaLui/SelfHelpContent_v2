<properties
	pageTitle="Check for errors in blobs and containers"
	description="Check for errors in blobs and containers"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32602738"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3d8aaec1-a13d-42c5-aecb-c0af447e3bbb"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check for errors in blobs and containers

You may execute the following query in order to retrieve the Blob related errors for a Storage Account.
Note: The following Table has only errors logged, therefore successful operations won't show here.

1. In Jarvis/MDM access the Logs section.
2. Complete the query details. The link is below.

~~~powershell
Namespace: Xstore
Events: FrontEndSummaryPerfLogs
Tenant: $StorageCluster
Role:  Nephos.Blob
Time range:Time range of the issue
Filtering: Account contains $StorageAccountName
~~~

 Useful information to check:
  1. **Operation**(Read/Write/Other)
  2. **RequestUrl**: has the information of the target Uri being accessed, in our case the complete path to the affected Blob.
  3. **HttpStatusCode**: For additional reference follow this List of HTTP status codes
  4. **Status**: reason for the failure being logged. Examples: 'SnapshotsPresent', 'LeaseIdMissing'
  5. **InternalStatus**: internal reason for the failure being logged. Example: 'ClientOtherError'.
  6. **UserAgent**: client the customer is using to perform the operation such as .NET, PowerShell, Azure CLI, etc.
  7. **ClientIP**: IP and Port of the client doing the operation.

**Recommended Documents**

1. [List of HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)
2. [Jarvis Logs](https://jarvis-west.dc.ad.msft.net/4ECD880C)
