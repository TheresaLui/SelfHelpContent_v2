<properties 
    pageTitle="I can't configure a new continuous export"
    description="I can't configure a new continuous export"
    service="microsoft.insights"
    resource="components"
    authors="mcosner"
    displayOrder="12"
    selfHelpType="resource"
    productPesIds="15693"
    cloudEnvironments="public"
 />
# I can't configure a new continuous export
## **Recommended steps**
To ensure that you are able to successfully configure a new continuous export rule:

1. Verify that the storage account is configured correctly.  It is required that you have write access to the storage account that you wish to configure a new continuous export for.  Premium storage accounts are not supported for continuous export.
2. Visual Studio subscribers, such as MSDN or BizSpark subscriptions, are required to attach a payment instrument and [remove their spending limit](https://go.microsoft.com/fwlink/?linkid=834519) prior to being allowed to start a continuous export.  It's important to remember to remove this **​indefinitely**, not just for the current billing period.  Continuous export rules configured in the Basic pricing tier will incur additional charges for exporting data.

## **Recommended documents**
[Understand how to export telemetry from Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-export-telemetry)<br>
[Understand how to use monthly Azure credits for Visual Studio subscribers](https://go.microsoft.com/fwlink/?linkid=834522)​