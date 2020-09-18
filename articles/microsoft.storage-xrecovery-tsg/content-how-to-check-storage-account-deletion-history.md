<properties
	pageTitle="How to check storage account deletion history"
	description="How to check storage account deletion history"
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
	articleId="baf872c8-6fdc-4269-9cc5-30f625bb03e0"
/>

# How to check storage account deletion history

**Important: Account name should not have been reused. **

Customer should NOT recreate a storage account with the same name. In some cases, recreating a storage account with the same name will cause the original storage account data to be cleaned up early making it unrecoverable. If already recreated, they will need to delete the recreated account before we start.

**Ensure storage account does not exist currently. (Use any one of the 2 options provided)**

None of the following should resolve.

	SET SA={StorageAccountName}
	nslookup %SA%.blob.core.windows.net
	nslookup %SA%.file.core.windows.net
	nslookup %SA%.table.core.windows.net
	nslookup %SA%.queue.core.windows.net

**Determine when storage account was deleted:**

Note: There might be multiple delete operations so you must carefully determine the relevant one. It typically is the earliest delete operation but always double check with customer.

**Option 1: Using a Kusto Query**

1. [Web Kusto Query Link](https://dataexplorer.azure.com/clusters/armprod/databases/ARMProd?query=H4sIAAAAAAAAA6VSwY7TMBC99yssnxIpSgEhDqyKFNKwRNo2VZzCsXLt2dRsGwd7Qne18O/YTbspapGQyMWK582b5/dmC0hYt87lhD670wqjWlS6WeXTX/RmtPXlZM534OuoDa9hlQihuwZX/voEStisaHvcNLvLqmzMlh9ZWuaLKi/mbFxmrFiWaXZbFssFGy/K4ks+zUo2nuVpWbDiUxWndwljecqqokxuXX9/JmlaLOcVG9Mb0k8q/3vS30eMxLazCCag3Oxao2X84P51vFeN1HsbN4A0jCVHvuYWAurELBzK3X1GbIsOa62auoTvHVi0I/KT7DdggCwMCGWhUjtgyHct+UAIr3Xw+q0MyQCzZwnkkkwmfTZnCN2C4b7sHfCAF+OJNleqJ7MGBuSmBlwaRYRukKvGBn3CIeGNJBW3D4du64Bo9wo3hF55XNbIr65GPTE8IrjW434c16N6ap0EotR98Kes09hBekTTLbdWCRp5R2k4IscvIgZq1zj5JxpvHxqnMbBgfigBR625jF5FLkF41PeXJfqehuFZ70ZbPNANPS9XNDbWtA5/LtFb5lLFzk4GlpOP0Zt3offILdM3EHixCdEV206vPqeOhuBGh6lCGwNb3q9KRC6eRTYutL431dJxwqOAw2bNwFo30KvSRoIh66fLBeVW/AbHNIpQHAQAAA==)


~~~kusto

let SubId="{Subscription_ID}";
let SAName="{Storage_Account_Name}";
let ASMOpName="DELETE/SUBSCRIPTIONS/RESOURCEGROUPS/PROVIDERS/MICROSOFT.CLASSICSTORAGE/STORAGEACCOUNTS/"; 
let ARMOpName="DELETE/SUBSCRIPTIONS/RESOURCEGROUPS/PROVIDERS/MICROSOFT.STORAGE/STORAGEACCOUNTS/";
cluster("armprod.kusto.windows.net").database("ARMProd").HttpOutgoingRequests
	| where PreciseTimeStamp >  ago(14d) 
	| where subscriptionId == SubId 
	| where operationName == ASMOpName or operationName == ARMOpName
	| where targetUri contains(SAName) and TaskName startswith "HttpOutgoingRequestEndWith"
	| extend StorageAccountType = iif(operationName contains ASMOpName, "Classic", "ARM")
		, region=iif(operationName contains ASMOpName
		, substring(serviceRequestId,0,indexof(serviceRequestId,":"))
		, substring(hostName,0,indexof(hostName,".rsrp"))
			)
		, TaskStatus=substring(TaskName,26)
	| project PreciseTimeStamp, StorageAccountType, region, TaskStatus, targetUri
	, correlationId, serviceRequestId, httpStatusCode, exceptionMessage
	| order by PreciseTimeStamp asc

~~~


Record the storage account type, region, delete timestamp and CorrelationID. We will need that in later steps.

**Option 2 : Using the ASC operations report.**

1. Navigate to [Resource Explorer in Azure Support Center ](https://azuresupportcenter.msftcloudes.com/resourceExplorer?srId=) and select the resource at the Subscription level(top resource).
2. Choose the operations tab, set the timeframe when the account might have been deleted. 
3. If not sure, choose last 14 days. Older deletes are unlikely to be recoverable.
4. Run the report.
