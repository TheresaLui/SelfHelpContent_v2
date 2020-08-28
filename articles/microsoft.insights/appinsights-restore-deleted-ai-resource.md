<properties 
    pageTitle="I need to restore deleted Application Insights Resource"
    description="What to do if my Application Insights resource was accidentally deleted"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729601"
    cloudEnvironments="public, Fairfax, mooncake, usnat, ussec"
    articleId="appinsights-restore-deleted-ai-resource"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# I need to restore an Application Insights resource that was accidentally deleted

## **Recommended Steps**

Deleted Application Insight resources (components) and their data most often can be recovered but there are criteria that must be met:
  
  1. The Application Insights component was deleted less than 30 days ago. You can check this in the **Azure Activity Logs** by searching for operation name *Delete insights component*
  1. The original subscription containing the deleted Application Insights component must still exist
  1. The resource group that contained the deleted application insights component must exist. If the resource group does NOT exist, recreating a new resource group with the same name will be required

**IMPORTANT:** Do NOT create another Application Insights resource with the name of the deleted resource. The recovery will not be possible if another Application Insights resource was created with the name that matches previously deleted Application Insights resource.

Continue forward with creation of the support ticket and a support engineer will help facilitate the recovery. Please provide the name of the deleted component, the resource group that contained it, and the subscription ID in the *Details* step to help moving the process more quickly.

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Manage Application Insights resources programmatically](https://docs.microsoft.com/azure/azure-monitor/app/powershell)
