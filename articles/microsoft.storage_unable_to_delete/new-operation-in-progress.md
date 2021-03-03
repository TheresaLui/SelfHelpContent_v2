<properties
	pageTitle="An operation is currently performing"
	description="An operation is currently performing"
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
	articleId="be56be63-ca12-4e4b-9339-bca04ba34c19"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# An operation is currently performing

To investigate the issue further, we need to find the details for the recent operation where the error message was received. From the recent failed operation details, we will be able to track the information for the operation that has the lock on the Storage Account. Finally, the lock operation will be reviewed and we'll take action depending on the lock reason

The objective of this section is finding the failed operation details, mainly **CorrelationId** and **Timeframe**. If you already have that information you may proceed to the next section:
## A) Identify the recent operation failure
Choose a method to find out the details of the failed operation:
### Option 1: Use ASC
1. Navigate to [Azure Support Center (ASC)](https://azuresupportcenter.msftcloudes.com/resourceExplorer) with the appropriate case number
2. Navigate to the Subscription level and select **Operations tab**
3. Select the approximate or exact timeframe of the issue and run the query
4. For **ARM**, the relevant information should be in the **ARM Operations** section
5. For **ASM**, the relevant information should be in the **RDFE Operations** section
6. You may filter further the results by completing some of these properties:
	1. Operation Name: operation that the customer is performing. For example: *Microsoft.Storage/storageAccounts/delete*
	2. Status: current progress or result of the operation such as Succeeded, Accepted, ***Failed***, Started, etc
	3. Resource Name: name of the Storage Account affected
	4. Resource Group: resource group where the Storage Account resides
7. When the relevant operation is found, take note of the **timeframe of the operation**(Event Time) and **CorrelationId**

### Option 2: Use Kusto
1. Get/Open [Kusto.Explorer](http://kusto/ke/Kusto.Explorer.application) . More information at [Tools reference](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2fGeneralPages%2fAzure%2fAzure_Virtual%20Machine_Tools%20reference).
2. Open a New Query Tab and Select the Armprod>ARMProd Connection
3. Fill the following example queries with your environment details to get further information. ShoeboxEntries Kusto Query([Example]()):

Execute: [Web](https://dataexplorer.azure.com/clusters/armprod.kusto.windows.net/databases/ARMProd?query=H4sIAAAAAAAEAFWPQWrDQAxF94XeQXiTBExLL1DwIgUvXEztCygzH3uKPTIaDemih%2b%2b4odBo%2bfX1eHJLTgY9HhpdNxV%2fOD15Nr5wQsk%2buv6WDbPgIl%2fnaBqQHh%2bozDddZyhIkSSrQ%2bsJ0adrsJmq58FEeULjnORo77yiuj8b2%2b48jE3X0yvxJMcXfyKOfsflxYYwRbZcejMnqt44LPAV%2fSGK6iecUa9wIWEMKwbjdaP6v05NskHZgsRd4La8g9c7qXSsfFWTE1Usv%2f3W%2fwBTalJBGgEAAA%3d%3d) | [Desktop](https://armprod.kusto.windows.net/ARMProd?query=H4sIAAAAAAAEAFWPQWrDQAxF94XeQXiTBExLL1DwIgUvXEztCygzH3uKPTIaDemih%2b%2b4odBo%2bfX1eHJLTgY9HhpdNxV%2fOD15Nr5wQsk%2buv6WDbPgIl%2fnaBqQHh%2bozDddZyhIkSSrQ%2bsJ0adrsJmq58FEeULjnORo77yiuj8b2%2b48jE3X0yvxJMcXfyKOfsflxYYwRbZcejMnqt44LPAV%2fSGK6iecUa9wIWEMKwbjdaP6v05NskHZgsRd4La8g9c7qXSsfFWTE1Usv%2f3W%2fwBTalJBGgEAAA%3d%3d&web=0) | [Web (Lens)](https://lens.msftcloudes.com/v2/#/discover/query//results?datasource=(cluster:armprod.kusto.windows.net,database:ARMProd,type:Kusto)&query=H4sIAAAAAAAEAFWPQWrDQAxF94XeQXiTBExLL1DwIgUvXEztCygzH3uKPTIaDemih%2b%2b4odBo%2bfX1eHJLTgY9HhpdNxV%2fOD15Nr5wQsk%2buv6WDbPgIl%2fnaBqQHh%2bozDddZyhIkSSrQ%2bsJ0adrsJmq58FEeULjnORo77yiuj8b2%2b48jE3X0yvxJMcXfyKOfsflxYYwRbZcejMnqt44LPAV%2fSGK6iecUa9wIWEMKwbjdaP6v05NskHZgsRd4La8g9c7qXSsfFWTE1Usv%2f3W%2fwBTalJBGgEAAA%3d%3d&runquery=1) | [Desktop (SAW)](https://armprod.kusto.windows.net/ARMProd?query=H4sIAAAAAAAEAFWPQWrDQAxF94XeQXiTBExLL1DwIgUvXEztCygzH3uKPTIaDemih%2b%2b4odBo%2bfX1eHJLTgY9HhpdNxV%2fOD15Nr5wQsk%2buv6WDbPgIl%2fnaBqQHh%2bozDddZyhIkSSrQ%2bsJ0adrsJmq58FEeULjnORo77yiuj8b2%2b48jE3X0yvxJMcXfyKOfsflxYYwRbZcejMnqt44LPAV%2fSGK6iecUa9wIWEMKwbjdaP6v05NskHZgsRd4La8g9c7qXSsfFWTE1Usv%2f3W%2fwBTalJBGgEAAA%3d%3d&saw=1)

https://armprod.kusto.windows.net/ARMProd
<!-- csl: https://armprod.kusto.windows.net -->
```kusto
cluster('Armprod').database('ARMProd').ShoeboxEntries
    | where resourceId endswith "/StorageAccountName"
    | where TIMESTAMP > ago(1d) and resultSignature has "Failed" 
    | project PreciseTimeStamp , resourceId , operationName , resultSignature , properties, correlationId
```
4. Review the details of the query, take note of the **CorrelationId** and **Timestamp** and navigate to the next section "***Review the details of the recent failed operation***" to find more information about the issue

## B) Review the details of the recent failed operation
**Review the details of the recent failed operation**
1. Open **Jarvis Logs/MDM**  and complete the query with the below details. [Query Example](https://jarvis-west.dc.ad.msft.net/F5E7D3D5):

~~~jarvis

Endpoint: Diagnostics PROD
Namespace: RegionalSRP
Events: ServiceApiQosEvent, ServiceBackgroundActivityEvent, ServiceConfigurationActivityEvent, ServiceContextActivityEvent, ServiceOperationActivityEvent, ServiceSystemActivityEvent
Region:  $AzureRegion$
Time range:$Timestamp$
Filtering: AnyField contains $CorrelatioId$

~~~

2. Within the query results start searching for the conflicting lock operation. Example below: ***Tip***: You may filter the search for TraceLevel below or equal than 4 to reduce the relevant logs
~~~jarvis
Unable to acquire Exclusive Account lock 'StorageAccountName'. Conflicting locks: c7037f26-91ad-4913-8933-838f6d6037ed[2018-09-10T19:55:06.8355897Z]"
~~~
## C) Review the details of the operation with the exclusive lock
1. Using Jarvis/MDM
2. Use the same query in the previous section but now use the **OperationId and Timestamp of the locking operation** found earlier
3. Within the query results start searching for the failure reason of the locking operation. Some examples below: ***Tip***: You may filter the search for TraceLevel below or equal than 4 to reduce the relevant logs
4. Once the error/cause of the issue found:
   1. If the error message implies a trivial resolution or it's actionable, please select Yes below
   2. Otherwise, select No below

## **Recommended Documents**

* [An operation is currently being performed](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265656/Azure_Storage_TSG_An-operation-is-currently-performing-on-this-storage-account-that-requires-exclusive-access)


