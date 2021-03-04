<properties
  pagetitle="V2 - Alerts Common Solutions"
  description="V2 - Alerts Common Solutions"
  service=""
  resource=""
  ms.author="chez,golamo"
  selfhelptype="Generic"
  supporttopicids="32629438"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="df5dec5b-0bba-43aa-970b-86ab340261eb"
  ownershipid="AzureData_DataFactory" />
# V2 - Alerts Common Solutions

## **Recommended Steps**

There are 2 ways to raise alerts for Azure Data Factory.

1. Raise alerts within Data Factory:

    1. This allows users to monitor activities within _one_ factory
    1. You can set up the alerts from your Data Factory UI
    1. Document: [Set Up Alerts](https://docs.microsoft.com/azure/data-factory/monitor-visually#alerts)

1. Raise alerts through Azure Monitor:

    1. This allows you to monitor activities across _multiple_ factories
    1. You need to integrate with Azure Monitor to utilize the features
    1. Alert state needs to be reset to _Closed_ once fired, otherwise successive issue would not raise new alert. More resource is here [Manage alerts](https://docs.microsoft.com/en-us/azure/azure-monitor/alerts/alerts-overview#manage-alerts)
    1. Documents: [Monitor Metrics with Azure Monitor](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#monitor-data-factory-metrics-with-azure-monitor) and [Set Up Alerts](https://docs.microsoft.com/azure/data-factory/monitor-visually#alerts)
	1. Subjects to rate limit as described in [Azure Monitor service limits](https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits)

## **Recommended Documents**

* Monitor visually [Document](https://docs.microsoft.com/azure/data-factory/monitor-visually), including following sections:

  * [Monitor Pipelines](https://docs.microsoft.com/azure/data-factory/monitor-visually#select-a-data-factory-to-monitor)
  * [Promote User Properties to Monitor](https://docs.microsoft.com/azure/data-factory/monitor-visually#promote-user-properties-to-monitor)
  * [Gantt Views](https://docs.microsoft.com/azure/data-factory/monitor-visually#gantt-views)
  * [Alerts](https://docs.microsoft.com/azure/data-factory/monitor-visually#alerts)

* Monitor with Azure Monitor [Document](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor), including following sections: 

  * [Logs and Event Schema](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#schema-of-logs-and-events)
  * [Integration with Azure Monitor and Log Analytics](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#monitor-data-factory-metrics-with-azure-monitor)
  * [Alerts](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#alerts)
  * [Azure Monitor service limits](https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits)
  * [Manage alerts](https://docs.microsoft.com/en-us/azure/azure-monitor/alerts/alerts-overview#manage-alerts)

**FAQ**

* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)