<properties
  pagetitle="**I expected an ITSM action to trigger, but it did not or was not received appropriately**&#xD;"
  service=""
  resource=""
  ms.author="yagil,nolavime"
  selfhelptype="Generic"
  supporttopicids="32739780,32745404"
  resourcetags=""
  productpesids="15454,15725"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alerts-notification-itsm"
  ownershipid="AzureMonitoring_ActionGroup" />
# **I expected an ITSM action to trigger, but it did not or was not received appropriately**

The IT Service Management Connector (ITSMC) allows you to connect Azure to a supported IT Service Management (ITSM) product/service.

## **Recommended Steps**

If you believe your ITSM connector did not send the alert properly, the following steps may help resolve the issue.

* Review the type of elements in the ITSM products from Azure alerts: The element types can be **Alert**, **Incident** or **Event**. You can change the type in the action [definition](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview#create-itsm-work-items-from-azure-alerts).
* Review the configuration item checkbox in order to create a configuration item. Configuration items are only supported in log alerts.
* From the ServiceDesk workspace, select **Create New Configuration Item in ITSM Product** in the ITSM connection.
* Make sure that your region is part of the supported regions for ITSM: ITSM Supported regions: East US, West US2,South Central US, West Central US, Central Canada, West Europe, South UK, Southeast Asia, East Japan, Central India, Southeast Australia. ITSM connections are not supported in other regions.
* If your tickets are not being created, or if your token expired in the ITSM provider (which happens every 30 days), do a [manual sync](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-resync-servicenow) is needed   
* Review the checkbox of the individual work items for each configuration item
* To have duplicate incidents for every update of the alert, select **Create Individual work items for each Configuration Item** in the ITSM action definition
* To have one incident that gets updated with every update of the ticket, you must deselect **Create Individual work items for each Configuration Item** in the ITSM action definionetion
* Check the [Dashboard](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-dashboard) to see if it contains common errors that can be solved.

## **Recommended Documents**

* [Connect Azure to ITSM tools using IT Service Management Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview)
* [Connect ITSM products/services with IT Service Management Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections)
* [Troubleshooting problems in ITSM Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-troubleshoot-overview)
