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

The IT Service Management Connector (ITSMC) allows you to connect Azure and a supported IT Service Management (ITSM) product/service.

## **Recommended Steps**

If you believe your ITSM connector did not sent the alert properly, the following steps might help resolve the issue.

* Review the type of elements in the ITSM products from Azure alerts:
The element types can be Alert, Incident or Event. You can change it in the action [definition](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview#create-itsm-work-items-from-azure-alerts).
* Review the configuration item checkbox in order to create configuration item:
Configuration item supported only in log alerts
* Check the checkbox of "Create New Configuration Item in ITSM Product" in the ITSM connection (in the ServiceDesk workspace)
* Review that your region is part of the supported regions for ITSM:
ITSM Supported regions: East US, West US2,South Central US, West Central US, Central Canada, West Europe, South UK, Southeast Asia, East Japan, Central India, Southeast Australia. Notice that ITSM connections does not supported in other regions.
* have connection issues tickets are not being created or your token has been expired  in the ITSM Product. How can I fix this?
This means that Refresh token have expired. The token expires every 30 days. Manual sync is needed in the connection UI:

    1. In Azure portal, go to All Resources and look for ServiceDesk(YourWorkspaceName)
    2. Under WORKSPACE DATA SOURCES click ITSM Connections
    3. Check that Please check your [configuration](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview). There might be misconfiguration:

        * [Connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-1): URL, Username/Password, Client ID/Client Secret
        * [User roles](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#create-integration-user-role-in-servicenow-app)
        * [Oauth Connection definition](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#prerequisites-1)

    4. Click on Sync

* Review the checkbox of the Individual work items for each Configuration Item
* In order to have duplicate incidents per every update of the alert you need to check the checkbox of "Create Individual work items for each Configuration Item" in the ITSM action definition.
* In order one incident that is updated in every update of the ticket you need to unchecked the checkbox of "Create Individual work items for each Configuration Item" in the ITSM action definition.

## **Recommended Documents**

* [Connect Azure to ITSM tools using IT Service Management Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview)
* [Connect ITSM products/services with IT Service Management Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections)
