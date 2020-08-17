<properties
	pageTitle="Check for errors for storage"
	description="Check for errors for storage"
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
	articleId="e9d66480-f423-405b-9e89-256adaeb1bae"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check for errors for storage

1. Open up Kusto or Kusto.WebExplorer to https://armprod.kusto.windows.net:443/ARMProd
2. Edit the StorageAccount name and adjust the time range parameters and run the following query:

~~~kusto

ShoeboxEntries | where resourceId contains '/StorageAccountName'| where TIMESTAMP > ago(1d) and resultType == 'Failure' | project PreciseTimeStamp , resourceId , operationName , resultSignature , properties, correlationId

~~~

3. When the relevant operation is found, take note of the timeframe of the operation(PreciseTimeStamp) and CorrelationId.

**Recommended Documents**

1. [Jarvis Kusto](https://jarvis-west.dc.ad.msft.net/logs/kusto)
2. [ARMProd Kusto](https://armprod.kusto.windows.net:443/ARMProd)
