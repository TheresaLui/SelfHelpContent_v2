<properties 
    pageTitle="I want to undelete an Application Insights resource"
    description="I want to undelete an Application Insights resource"
    service="microsoft.insights"
    articleId="insights-deletedresource"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    displayOrder="216"
    selfHelpType="generic"
    supportTopicIds="32632992, 32633000"
    productPesIds="15693"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I want to undelete an Application Insights resource

## **Recommended Steps**

Application Insights performs a soft-delete on resources so there is a good chance we still have your data, but you need to act fast. To undelete an Application Insights resource you will need to make sure of the following prerequisites.<br>

1. A resource has not been created with the same name
2. The resource group still exists
3. You know the resource name or instrumentation key

**Known Issues**<br>

1. If the resource has been recreated we cannot recover it
2. If you've purged data and want it back you cannot do that as there is no soft-delete for actual data