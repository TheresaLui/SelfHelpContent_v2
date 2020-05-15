<properties
    pageTitle="ITSM action didn't trigger as expected"
    description="Expected an ITSM action to trigger, but it did not trigger or was not received appropriately"
    infoBubbleText=""
    service="microsoft.insights"
    resource="actiongroups"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-notification-itsm"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739780"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# **I expected an ITSM action to trigger, but it did not or was not received appropriately**

The IT Service Management Connector (ITSMC) allows you to connect Azure to a supported IT Service Management (ITSM) product/service.

## **Recommended Steps**

If you believe your ITSM connector did not send the alert properly, the following steps may help resolve the issue.

* Review the type of elements in the ITSM products from Azure alerts:
The element types can be Alert, Incident or Event. You can change it in the action [definition](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview#create-itsm-work-items-from-azure-alerts).
* Review the configuration item checkbox in order to create configuration item:
Configuration item supported only in log alerts
* Check the checkbox of "Create New Configuration Item in ITSM Product" in the ITSM connection (in the ServiceDesk workspace)
* Review that your region is part of the supported regions for ITSM:
ITSM Supported regions: East US, West US2,South Central US, West Central US, Central Canada, West Europe, South UK, Southeast Asia, East Japan, Central India, Southeast Australia. Notice that ITSM connections are not supported in other regions.
* If your tickets are not being created, or your token has expired in the ITSM provider (which happens every 30 days), [manual sync](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-resync-servicenow) is needed. 
   
* Review the checkbox of the Individual work items for each Configuration Item
* In order to have duplicate incidents per every update of the alert you need to check the checkbox of "Create Individual work items for each Configuration Item" in the ITSM action definition.
* In order to have one incident that is updated per every update of the ticket, you need to uncheck the checkbox of "Create Individual work items for each Configuration Item" in the ITSM action definition.

## **Recommended Documents**

* [Connect Azure to ITSM tools using IT Service Management Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview)
* [Connect ITSM products/services with IT Service Management Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections)
