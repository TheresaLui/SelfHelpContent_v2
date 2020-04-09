<properties
	articleId="130f32d5-3308-4531-8608-c68b3e7ec1c5"
	articleTags="costmanagement,scheduled exports,exports"
	pageTitle="I got an error when setting up a scheduled export."
	description="scheduled-exports-error"
	displayOrder="5"
	authors="shasulin"
	ms.author="shasulin"
	selfHelpType="resource"
	service="microsoft.costmanagement"
	resource="exports"
	resourceTags=""
	productPesIds="15659"
	supportTopicIds=""
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	ownershipId="ASMS_Billing"
/>

# I got an error when setting up a scheduled export

There are multiple reasons why you are getting an error when scheduling an export, let’s go through them to troubleshoot your errors:<br>

<b>Do you have the necessary permissions to set up a storage account?</b><br>
You need to have contributor or owner access to the subscription you have selected in order to create a new storage account.<br>

<b>Do you have necessary permissions to access the storage account?</b>  <br>
Exports checks for authentication for accessing the storage account in order to dump the usage files. <br>
You need to have reader, contributor or owner access to the storage account in order to create the export to an existing storage account.

<b>Is the selected subscription present in your tenant?</b><br>
Exports supports subscriptions that are present in your own tenant and not across tenants. <br> 
For eg. A lighthouse partner cannot create an export using a customer’s subscription they have access to. The subscriptions needs to be a separate PAYG subscription in the partner tenant.  

<b>Does the selected storage account exist in the same resource group?</b><br>

If the location of a storage account has moved from the selected resource group to another resource group, creation as well as created exports will be unable to access the storage account to export the data. <br>  

## **Recommended Documents**

* [Create and manage exported data](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-export-acm-data#create-a-daily-export)<br>
* [Verify data collection](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-export-acm-data#verify-that-data-is-collected)<br>
