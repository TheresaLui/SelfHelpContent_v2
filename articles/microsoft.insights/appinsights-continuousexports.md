<properties 
    pageTitle="Issue exporting telemetry with Continuous export"
    description="Troubleshooting guide for exporting telemetry with Continuous exports"
    service="microsoft.insights"
    resource="components"
    authors="sdash"
    ms.author="sdash"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729608"
    cloudEnvironments="public, Fairfax, mooncake, usnat, ussec"
 	articleId="appinsights-continuousexports"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Issue exporting telemetry with Continuous export

## **Recommended Steps**

If you have issues configuring Continuous export, please note the following:

1. To add or change exports, you need Owner, Contributor, or Application Insights Contributor access rights.
2. If you change the key to your storage, continuous export will stop working. You'll see a notification in your Azure account.
Open the Continuous Export tab and edit your export. Edit the Export Destination, but just leave the same storage selected. Click OK to confirm. The continuous export will restart.
3. Continuous export is only supported for classic Application Insights resources. [Workspace-based Application Insights resources](https://docs.microsoft.com/azure/azure-monitor/app/create-workspace-resource) must use [diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/app/create-workspace-resource#export-telemetry). Exports via diagnostic settings are significantly faster, have the same schema as what you see on Log Analytics etc.
4. Continuous export does not support use of VNET/Azure Storage firewalls in conjunction with Azure Blob storage, or Azure Data Lake Storage Gen2.
5. Once you've created your export, newly ingested data will begin flowing to the Azure Blob storage in about an hour. Any data that existed prior to enabling continuous export will not be exported, and there is no supported way to retroactively export previously created data using continuous export.
6. If your application sends a lot of data, the sampling feature may operate and send only a fraction of the generated telemetry. See [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling) to configure sampling from your code for the specific SDK implementation you are using and the kind of sampling you wish to configure.
7. To pause exports, click on Disable. To stop the export permanently, delete the continuous export (doing so doesn't delete your data from storage). 


## **Recommended Documents**
* [Using Continuous exports](https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport?view=azps-4.4.0)<br>
* [Application Insights export data model](https://docs.microsoft.com/azure/azure-monitor/app/export-data-model)<br>