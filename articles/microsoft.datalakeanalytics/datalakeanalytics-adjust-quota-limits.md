<properties
    pageTitle="Adjusting Azure Data Lake Analytics Quotas"
    description="Manage Quotas on Azure Data Lake Analytics"
    service="Microsoft.DataLakeAnalytics"
	resource="accounts"
	authors="guyhay"
    ms.author="guyhay"
	displayOrder="8"
	selfHelpType="resource"
	productPesIds="15940"
   	supportTopicIds="32680642"
	cloudEnvironments="public, Fairfax, usnat, ussec"
   	articleId="datalakeanalytics-adjust-quota-limits"
		ownershipId="AzureData_AzureDataLakeAnalytics"
/>

# Manage Quotas on Azure Data Lake Analytics

Quotas define the limits of Azure Data Lake Analytics compute resources that a subscription or Azure Data Lake Analytics account can provision or consume. For example, a quota could allow up to five Azure Data Lake Analytics accounts in a region. Each resource can have its own quota.

Common quota requests include:

* Increasing the number of ADLA accounts from the default of 5 per subscription and region
* Increasing the maximum number of concurrent AUs per ADLA account from the default of 250 per ADLA account
* Increasing the maximum number of concurrent jobs per ADLA account from the default of 20 per ADLA account

Quota increases have the potential to increase your AU consumption and therefore your monthly bill.

## **Recommended Steps**

1. If you want to lower these values, you can do that yourself in the Limits and policies of the ADLA portal blade
2. If you want to increase the number of Azure Data Lake accounts, please provide a subscription GUID and region. These items must exist prior to creating the increase request.
3. If you want to increase the maximum number of concurrent AUs, or the maximum number of concurrent jobs, please provide the subscription GUID, ADLA account name, and region. These items must exist prior to creating the increase request.

## **Recommended Documents**

* [Learn about Azure Data Lake Analytics quotas and limits](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-quota-limits)<br>
* [Learn about Azure Data Lake Analytics policies](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-policies)<br>
* [Learn about account-level policies and job-level policies](https://blogs.msdn.microsoft.com/azuredatalake/2017/06/08/managing-your-azure-data-lake-analytics-compute-resources-overview/)<br>
