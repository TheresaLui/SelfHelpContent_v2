<properties
	pageTitle="scheduled reports functionality"
	description="scheduled reports functionality"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32615298,32615297"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
	articleId="9af7896e-f094-4405-8449-c79778dcf15b"
/>

# Scheduled reports functionality

Daily recurring tasks can be created that automatically exports the Cost Management data to Azure storage. Exported data is in CSV format and it contains all the information that's collected by Cost Management. This exported data can then be combined with other data and integrated into external systems like a dashboard or other financial system

Please note that export is available to all [Enterprise Agreement (EA)](https://azure.microsoft.com/pricing/enterprise-agreement/) customers

## Prerequisites:
Add all users who will be setting up recurrent export tasks to one of the following roles:

* Subscription Owner – Can create, modify, or delete scheduled exports for a subscription.
* Subscription Contributor – Can create, modify, or delete their own scheduled exports. Can modify the name of scheduled exports created by others.
* Subscription Reader – Can schedule exports that they have permission to.

## How to create a daily report?

1. Sign in to [Azure portal](https://portal.azure.com)<br>
2. Select **Cost Management + Billing** and select a subscription or a resource group in the subscription. Then click **Export** and **Add**.<br>
3. Type a name for the export and specify the subscription, Azure storage account, container, and the file storage directory or blob container, then click **Create**.<br>
4. The new export will appear in the list of exports.<br>

*Note:* By default, new exports are enabled, and they run daily. If you want to disable or delete a scheduled export, click any item in the list and then click either **Disable** or **Delete**. Initially, it can take one to two hours before the export runs. However, it can take up to four hours before data is shown in exported files.<br>

## How to verify that the data is collected?

1. In the export list, click the storage account name.<br>
2. On the storage account page, click **Open** in Explorer. If you see a confirmation box, click **Yes** to open the file in Azure Storage Explorer. Download [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/)<br>
3. In Storage Explorer, navigate to the container that you want to open and select the folder corresponding to the current month. A list of CSV files is shown. Select one and then click **Open**.<br>
4. The file opens with the program or application that's set to open CSV file extensions.<br>

## **Recommended documents**

* [Create and Manage exported data](https://docs.microsoft.com/azure/cost-management/tutorial-export-acm-data)<br>
* [What is Azure Cost Management ?](https://docs.microsoft.com/azure/cost-management/overview-cost-mgt)<br>
* [Analyze your costs and spending](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management best practices](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>
* [Explore and analyze costs with Cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management - Pricing](https://azure.microsoft.com/pricing/details/cost-management/)<br>
