<properties
    pageTitle="Adjusting Azure Data Lake Analytics Quotas"
    description="Manage Quotas on Azure Data Lake Analytics"
    service="Microsoft.DataLakeAnalytics"
	resource="datalake"
	authoralias="guyhay"
	authors="guyhayMSFT"
    ms.author="guyhay"
	displayOrder=""
	selfHelpType="resource"
	productPesIds="15940"
    supportTopicIds="32680642"
	cloudEnvironments="public"
    articleId="datalakeanalytics-adjust-quota-limits"	
/>
# Manage Quotas on Azure Data Lake Analytics

Quotas define the limits of resources that a user subscription or Azure Data Lake Analaytics account can provision or consume. For example, a quota might allow a user to create up to five Azure Data Lake Analytics accounts. Each resource can have its own types of quotas.

## **Recommended Steps**

1. There are two types of common Azure Data Lake quota requests. Increasing the numbmer of Azure Data Lake Analytics accounts, or increasing the number of concurrent AUs or concurrent jobs
2. The default values for new Azure Data Lake accounts are 5 accounts, up to 250 AUs for each job and 20 concurrent jobs
3. If you want to lower these values, you can in the ADLA portal blade without creating a support incident
4. If you want to increase these values, please continue creating the support request  
5. If you want to increase the number of Azure Data Lake acoounts We will need the subscription GUID and region
6. If you want to increase the maximum number of concurrent AUs or maximum number of concurrent jobs we will need the subscription GUID, ADLA account name and region

## **Recommended Documents**

* [Adjust quotas and limits in Azure Data Lake Analytics](https://docs.microsoft.com/en-us/azure/data-lake-analytics/data-lake-analytics-quota-limits)<br>
