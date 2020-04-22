<properties
	articleId="9191c565-5c6e-4861-8b12-9f07afcafdde"
	articleTags="costmanagement,scheduled exports,exports"
	pageTitle="I scheduled an export, but I don’t get them anymore"
	description="scheduled-exports-stopped"
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

# I scheduled an export, but I don’t get them anymore

At the time of exporting every file, exports checks for the presence of the subscription, access to use the subscription, presence of the storage account in the resource group and access to read/write on the storage account using the credentials that were used to set up the export. <br>
If either of these fails or have been changed, the export job will fail and no new file will be dumped to the storage account.  

## **Recommended Documents**

* [Create and manage exported data](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-export-acm-data#create-a-daily-export)<br>
* [Verify data collection](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-export-acm-data#verify-that-data-is-collected)<br>
