<properties 
    pageTitle="I am seeing errors or latency with telemetry collection"
    description="I am seeing errors or latency with telemetry collection"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_collectionerrors"
    displayOrder="101"
    selfHelpType="generic"
    supportTopicIds="32602224"
    productPesIds="15693"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am seeing errors with telemetry collection

## **Recommended Steps**

For all supported SDKs you should not see any errors relating to telemetry collection. If you are seeing errors that are specific to **dc.services.visualstudio.com**, please use the steps below. If you are seeing other errors coming from your application, please go back and open a case for the SDK.

1. Verify the version of the SDK you are using is up to date or a [supported version](https://github.com/Microsoft/ApplicationInsights-Home#officially-supported-sdks)
2. Check the [Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) for warnings
3. If the errors are inside of your telemetry, please go back and open a case for the correct SDK
4. If you are receiving an error message from the service, it is likely that we are experiencing issues and it is recommended to open a case for tracking

## **Recommended Documents**

* [Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)
