<properties
	pageTitle="ADLS Gen 2 How to check storage account deletion history"
	description="How to check storage account deletion history"
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
	articleId="08c91d3c-9afa-477d-ada5-3a26e01de43e"
/>

# ADLS Gen 2 How to check storage account deletion history

**Important: Account name should not have been reused**

The customer should **not** recreate a storage account with the same name. In some cases, recreating a storage account with the same name will cause the original storage account data to be cleaned up early, making it unrecoverable. If the storage account is already re-created, they will need to delete the re-created account before we start.

**Ensure storage account does not exist currently**

None of the following should resolve.

	SET SA={StorageAccountName}
	nslookup %SA%.blob.core.windows.net
	nslookup %SA%.file.core.windows.net
	nslookup %SA%.table.core.windows.net
	nslookup %SA%.queue.core.windows.net

**Determine when storage account was deleted**

**Note.** There might be multiple delete operations, so you must carefully determine the relevant one. It typically is the earliest delete operation, but always double-check with the customer.

**Option 1 : Use the ASC operations report**

1. Navigate to [Resource Explorer in Azure Support Center ](https://azuresupportcenter.msftcloudes.com/resourceExplorer?srId=) and select the resource at the Subscription level(top resource).
2. Select the **Storage tab** section.
3. Fill the details of the Storage Account attempted to be recovered under the subsection Account Deletion History & Recovery
4. Add the deletion time if known (optional) 
5. Run the query


**Option 2: Use a Kusto Query**

1. [Web Kusto Query Link](https://dataexplorer.azure.com/clusters/armprod/databases/ARMProd?query=H4sIAAAAAAAAA6VSwY7TMBC99yssnxIpSgEhDqyKFNKwRNo2VZzCsXLt2dRsGwd7Qne18O/YTbspapGQyMWK582b5/dmC0hYt87lhD670wqjWlS6WeXTX/RmtPXlZM534OuoDa9hlQihuwZX/voEStisaHvcNLvLqmzMlh9ZWuaLKi/mbFxmrFiWaXZbFssFGy/K4ks+zUo2nuVpWbDiUxWndwljecqqokxuXX9/JmlaLOcVG9Mb0k8q/3vS30eMxLazCCag3Oxao2X84P51vFeN1HsbN4A0jCVHvuYWAurELBzK3X1GbIsOa62auoTvHVi0I/KT7DdggCwMCGWhUjtgyHct+UAIr3Xw+q0MyQCzZwnkkkwmfTZnCN2C4b7sHfCAF+OJNleqJ7MGBuSmBlwaRYRukKvGBn3CIeGNJBW3D4du64Bo9wo3hF55XNbIr65GPTE8IrjW434c16N6ap0EotR98Kes09hBekTTLbdWCRp5R2k4IscvIgZq1zj5JxpvHxqnMbBgfigBR625jF5FLkF41PeXJfqehuFZ70ZbPNANPS9XNDbWtA5/LtFb5lLFzk4GlpOP0Zt3offILdM3EHixCdEV206vPqeOhuBGh6lCGwNb3q9KRC6eRTYutL431dJxwqOAw2bNwFo30KvSRoIh66fLBeVW/AbHNIpQHAQAAA==)

```
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
```
Record the storage account type, region, delete timestamp, and `CorrelationID`. You'll need this information in later steps.

**Option 3: Geneva Actions**

1. In Geneva Actions, navigate to [SRP > SRP Operations > Get Deleted Storage Account](https://jarvis-west.dc.ad.msft.net/271CD959?genevatraceguid=d42c3a17-2955-489e-abfc-d4610df8017c)  
2. Fill in the requested information and click **Run**
3. Review all entries returned to determine the right version to be recovered

**Note:** "Account not found". This may be because of the following:

- The provided information is incorrect, or
- The deletion time was more than 14 days in the past (in which case the account cannot be recovered), or
- The account was a Microsoft.ClassicStorage account or RDFE account, which should be recovered with by running the classic account recovery ASC troubleshooter , or [TSG 1187811](http://vstfrd:8080/Azure/RD/_workitems?id=1187811&_a=edit) instead, or
- There is some issue with the Deleted Accounts list in SRP, in which case you can engage the XStore > Location Service DRI.
