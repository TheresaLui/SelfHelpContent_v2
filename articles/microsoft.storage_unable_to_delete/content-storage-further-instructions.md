<properties
	pageTitle="Storage migrating further instructions"
	description="Storage migrating further instructions"
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
	articleId="588742d4-ed50-4fce-8663-694d488c74bc"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Storage migrating further instructions

1. At this time the error message and failed Operation Ids should be clear. If not please collect the required information. Further guidance at [Unable to Delete - Internal Data Collection](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2fGeneralPages%2fAzure%2fAzure_Storage_Unable%20to%20Delete%20Workflow).
2. Proceed to execute the following Jarvis Query to find more information of the issue within the logs. Example Jarvis Query.

~~~jarvis

    Namespace: Rdfe
    Events: ServiceContextActivityEtwTable, RdfeExceptionEventEtwTable
    Time range:<Time range of the issue>
    Filtering: OperationId == <OperationId>

~~~

3. Review the logs and try to find the root cause of the issue. Tip: You may filter the search for Trace below or equal than 4 to reduce the relevant logs.
4. If the error message is different and actionable, guide the customer to resolve the issue. Note that at this time Commit and Abort operations should have been tried.
