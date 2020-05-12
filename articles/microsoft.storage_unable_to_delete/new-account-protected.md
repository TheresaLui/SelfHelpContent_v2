<properties
	pageTitle="The specified account is protected"
	description="The specified account is protected"
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
	articleId="bc9736ba-39ee-4b59-80f0-a1e1db77dcbc"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# The specified account is protected

1. At this time the error message and failed Operation Ids should be clear. If not please collect the information
2. Proceed to execute the following Jarvis Query to find more information of the issue within the logs

~~~Jarvis

Namespace: Rdfe
Events: ServiceContextActivityEtwTable, RdfeExceptionEventEtwTable
Time range:<Time range of the issue>
Filtering: OperationId == $operationid$

~~~

3. Review the logs and try to find the root cause of the issue.
4. If the error message is AccountProtectedFromDeletion select No below
5. If the error message is different and actionable, select Yes below

**Recommended Documents**

1. [AccountProtectedFromDeletion](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265692/Azure_Storage_TSG_The-specified-account-is-protected-from-deletion)
2. [Internal data collection](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2fGeneralPages%2fAzure%2fAzure_Storage_Unable%20to%20Delete%20Workflow)
3. [Known issues](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2fGeneralPages%2fAzure%2fAzure_Storage_Unable%20to%20Delete%20Workflow)
