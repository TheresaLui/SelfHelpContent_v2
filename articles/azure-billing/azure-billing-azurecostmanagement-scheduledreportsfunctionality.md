<properties
	pageTitle="scheduled reports functionality"
	description="scheduled reports functionality"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615298"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
/>

# Scheduled reports functionality

Daily recurring tasks can be created that automatically exports the Cost Management data to Azure storage. Exported data is in CSV format and it contains all the information that's collected by Cost Management. This exported data can then be used in Azure storage with external systems and be combined with custom data. Also the exported data can be used in an external system like a dashboard or other financial system

**Prerequisites**

Data export is available to all [Enterprise Agreement (EA)](https://azure.microsoft.com/pricing/enterprise-agreement/) customers. The following Azure permissions are supported per subscription for data export by user and group:

  * Owner – Can create, modify, or delete scheduled exports for a subscription.
  * Contributor – Can create, modify, or delete their own scheduled exports. Can modify the name of scheduled exports created by others.
  * Reader – Can schedule exports that they have permission to.
  
For Azure Storage accounts:

  * Write permissions are required to change the configured storage account, regardless of permissions on the export.
  * Your Azure storage account must be configured for blob or file storage.
	
**How to create a daily report ?**

1. Sign in to [Azure portal](azure-billing-azurecostmanagement-scheduledreportsfunctionality.md)
2. Select Cost Management + Billing > select a subscription or resource group in a subscription > Export > **Add**.
3. Type a name for the export and specify the subscription, Azure storage account, container, and the file storage directory or blob container, then click **Create**.
4. The new export will appear in the list of exports. <br>
	
*Note:* By default, new exports are enabled, and they run daily. If you want to disable or delete a scheduled export, click any item in the list and then click either Disable or Delete. Initially, it can take one to two hours before the export runs. However, it can take up to four hours before data is shown in exported files.
	
**How to verify that the data is collected ?**

1. In the export list, click the storage account name.
2. On the storage account page, click Open in Explorer. If you see a confirmation box, click **Yes** to open the file in Azure Storage Explorer.
3. In Storage Explorer, navigate to the container that you want to open and select the folder corresponding to the current month. A list of CSV files is shown. Select one and then click **Open**.
4. The file opens with the program or application that's set to open CSV file extensions.	


## **Recommended documents**

* [Create and Manage exported data](https://docs.microsoft.com/azure/cost-management/tutorial-export-acm-data)<br>
* [What is Azure Cost Management ?](https://docs.microsoft.com/azure/cost-management/overview-cost-mgt)<br>
* [Analyze your costs and spending](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management best practices](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>
* [Explore and analyze costs with Cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management REST API](https://docs.microsoft.com/rest/api/cost-management/)<br>
* [Azure Consumption REST API documentation](https://docs.microsoft.com/rest/api/consumption/)<br>
* [Azure Cost Management - Pricing](https://azure.microsoft.com/pricing/details/cost-management/)<br>
