<properties
	pageTitle="Quota Limit Reached"
	description="Quota Limit Reached"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0504479a-4194-4d1e-aeb0-42e4370507bc"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Quota limit reached (cores, public IPs,...) issue

Cluster startup failure due to Databricks is not able to acquire VMs.

**User facing error**: 
*Cloud Provider Launch Failure: A cloud provider error was encountered while setting up the cluster. See the Databricks guide for more information.*
*Azure error code: OperationNotAllowed*
*Azure error message: Operation results in exceeding quota limits of Core. Maximum allowed: xx, Current in use: xx, Additional requested: xx.*

## Troubleshooting and Solution

Go to cluster events tab, look for event when cluster fails and click on it to get more information.

To resolve the issue:

1. You can either *stop unused clusters* to release resources
2. Or if the first suggested solution is not feasible, please *open a case with Azure Subscription Management team* making sure to incluse these details: 
   Subscription ID, Region, VM type, Current available number of cores, Number of cores to be added
   
**Note:** Having customer fill out the form to raise a quota request is much faster than collab tasks to quota team. Sometimes these requests are instantly auto-approved.

Please check these documents for further details regarding:

* [Step by step on opening the case](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests)
* [Check resource usage against limits](https://docs.microsoft.com/azure/networking/check-usage-against-limits)

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [file an IcM](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/333941/Escalate-to-Product-Group-team) if needed.