<properties
	pageTitle="Cost Management - export errors"
	description="Cost Management - export errors"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32615297"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="9af7896e-f094-4405-8449-c79778dcf15b"
	ownershipId="ASMS_Billing"
/>

# Cost Management - export errors

* **I got an error when setting up a scheduled export**<br>
There are multiple reasons why you are getting an error when scheduling an export, let’s go through them to troubleshoot your errors: 

   1. **Do you have the necessary permissions to set up a storage account?**<br>
You need to have contributor or owner access to the subscription you have selected in order to create a new storage account<br>

   2. **Do you have necessary permissions to access the storage account?**<br>
Exports checks for authentication for accessing the storage account in order to dump the usage files. You need to have reader, contributor or owner access to the storage account in order to create the export to an existing storage account<br>

   3. **Is the selected subscription present in your tenant?**<br>
Exports supports subscriptions that are present in your own tenant and not across tenants. For eg. A lighthouse partner cannot create an export using a customer’s subscription they have access to. The subscriptions needs to be a separate PAYG subscription in the partner tenant<br>

   4. **Does the selected storage account exist in the same resource group?**<br>
If the location of a storage account has moved from the selected resource group to another resource group, creation as well as created exports will be unable to access the storage account to export the data<br>

* **I scheduled an export but I don’t get them anymore**<br>
At the time of exporting every file, exports checks for the presence of the subscription, access to use the subscription, presence of the storage account in the resource group and access to read/write on the storage account using the credentials that were used to set up the export. If either of these fails or have been changed, the export job will fail and no new file will be dumped to the storage account<br>

* **I got an empty scheduled exports file even though I had usage**<br>
This is usually because the exports job failed to pick up the data. We suggest you check for successive exports and if this repeat, please open a support ticket<br>

Please note Data export is available for a variety of Azure account types, including [Enterprise Agreement (EA)](https://azure.microsoft.com/pricing/enterprise-agreement/) and [Microsoft Customer Agreement customers](https://docs.microsoft.com/azure/cost-management-billing/costs/get-started-partners). To view the full list of supported account types, see [Understand Cost Management data](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-cost-mgt-data).<br>

### Prerequisites

Add all users who will be setting up recurrent export tasks to one of the following roles:

* Subscription Owner – Can create, modify, or delete scheduled exports for a subscription.
* Subscription Contributor – Can create, modify, or delete their own scheduled exports. Can modify the name of scheduled exports created by others.
* Subscription Reader – Can schedule exports that they have permission to.

Learn more: [Prerequisites](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-export-acm-data#prerequisites)

### Create a daily report

1. Sign in to [Azure portal](https://portal.azure.com)<br>
2. Select **Cost Management + Billing** and select a subscription or a resource group in the subscription. Then click **Export** and **Add**.<br>
3. Type a name for the export and specify the subscription, Azure storage account, container, and the file storage directory or blob container, then click **Create**
4. The new export will appear in the list of exports

*Note:* By default, new exports are enabled, and run daily. If you want to disable or delete a scheduled export, click any item in the list and then click either **Disable** or **Delete**. Initially, it can take one to two hours before the export runs. However, it can take up to four hours before data is shown in exported files.<br>

### Verify that the data is collected

1. In the export list, click the storage account name
2. On the storage account page, click **Open** in Explorer. If you see a confirmation box, click **Yes** to open the file in [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/).
3. In Storage Explorer, navigate to the container that you want to open and select the folder corresponding to the current month. A list of CSV files is shown. Select one and then click **Open**.<br>
4. The file opens with the program or application that's set to open CSV file extensions

## **Recommended Documents**

* [Create and Manage exported data](https://docs.microsoft.com/azure/cost-management/tutorial-export-acm-data)<br>
* [Azure Cost Management best practices](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>
* [Exports API](https://docs.microsoft.com/rest/api/cost-management/exports/createorupdate)<br>
* [What is Azure Cost Management?](https://docs.microsoft.com/azure/cost-management/overview-cost-mgt)<br>
* [Analyze your costs and spending](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Explore and analyze costs with Cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management: Pricing](https://azure.microsoft.com/pricing/details/cost-management/)<br>
