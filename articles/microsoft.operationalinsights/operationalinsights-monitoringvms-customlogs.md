
<properties
pageTitle="Custom logs and Data collector API"
description="Custom logs and Data collector API"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="operationalinsights-monitoringvms-customlogs"
symptomID=""
infoBubbleText=""
authors="evternov"
ms.author="evternov"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612533"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Custom logs and Data collector API

GUIDs and Strings are functionally equivalent in the Log Analytics back end.
While you may see an “_g” suffix for GUID fields, these GUIDs will be stored as a string data type. 
While we apply several indexing optimizations specific to the GUID format behind the scenes, fundamentally being a string, these “_g” fields will have all the same capabilities as any other “_s” string field.
This is expected behaviour. To learn more about type interpolation in the Data Collector API.

## **Recommended Documents**

* [Log data ingestion time in Azure Monitor](https://docs.microsoft.com/ azure/azure-monitor/platform/data-collector-api#record-type-and-properties)<br>
