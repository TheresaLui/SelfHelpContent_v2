
<properties
pageTitle="Customer-managed key (CMK)"
description="Customer-managed key (CMK)"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="operationalinsights_customer_managed_key_(cmk)"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder=""
selfHelpType="generic"
supportTopicIds="32745440"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Customer-managed key (CMK)

Some of the configuration operations run asynchronously because they can't be completed quickly. When using REST requests in configuration, the response initially returns an HTTP status code 200 (OK) and header with Azure-AsyncOperation property when accepted. [Learn more](https://docs.microsoft.com/azure/azure-monitor/platform/customer-managed-keys#asynchronous-operations-and-status-check)

## **Recommended Steps**

A description of Customer-managed key function and configuration is documented in [Customer-managed key article](https://docs.microsoft.com/azure/azure-monitor/platform/customer-managed-keys). Also review these:
* CMK (KEK) revocation -- Log Analytics cluster respect changes in key permissions within an hour or sooner
* CMK (KEK) rotation -- You must update Log Analytics cluster with new key key identifier details (URI, name and version). If you don't update the details in the Cluster resource, the Log Analytics cluster storage will keep using your previous key for encryption.
* Common issues -- review [troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/platform/customer-managed-keys#troubleshooting)<br>

## **Recommended Documents**

* [Customer-managed key article](https://docs.microsoft.com/azure/azure-monitor/platform/customer-managed-keys)
* [Asynchronous operations and status check when using REST requests](https://docs.microsoft.com/azure/azure-monitor/platform/customer-managed-keys#asynchronous-operations-and-status-check)
* [Troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/platform/customer-managed-keys#troubleshooting)<br>