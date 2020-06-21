<properties 
    pageTitle="Setting or changing a daily cap on ingestion"
    description="How to set or change a daily cap on ingestion"
    service="microsoft.insights"
    resource="components"
    authors="jgol"
    ms.author="MS-jgol"
    selfHelpType="generic"
    articleId="appinsights-ingestion-cap"
    productPesIds="15693"
    supportTopicIds="32632982"
    cloudEnvironments="public, Fairfax, mooncake, usnat, ussec"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
<!-- appinsights-set-daily-ingestion-cap -->

# **I need to change or set a daily cap on ingestion**

To change the daily cap, in the Configure section of your Application Insights resource, in the **Usage and estimated costs** page, select Daily Cap. Enter the maximum daily GB you want to allow, and click OK.  Use care when you set the daily cap. Your intent should be to never hit the daily cap. If you hit the daily cap, you lose data for the remainder of the day, and you can't monitor your application. [Learn more](https://docs.microsoft.com/azure/azure-monitor/app/pricing#manage-your-maximum-daily-data-volume) about managing your maximum daily data volume.

## **Recommended Documents**

* [Manage your maximum data volume](https://docs.microsoft.com/azure/azure-monitor/app/pricing#manage-your-maximum-daily-data-volume)