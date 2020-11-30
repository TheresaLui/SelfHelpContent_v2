<properties
  pagetitle="IoT Hub logging and metrics &#xD;"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,saziz,jtanner,yiygu"
  selfhelptype="Generic"
  supporttopicids="32630559"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="333e2e76-151c-46ca-82b0-4dea35d409fa"
  ownershipid="AzureIot_IotHub" />
# IoT Hub logging and metrics 

 

## **Recommended Steps** 

 

Have you enabled diagnostic settings for logs and metric? Without this step, you won't be able to use log analytics and monitor your data. Follow [collection and routing](https://docs.microsoft.com/azure/iot-hub/monitor-iot-hub#collection-and-routing) section of the monitoring tutorial to enable diagnostic settings. This workflow typically has a 15 minutes latency before you can view monitor data. 

Learn more about IoT Hub's [logging](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#understand-the-logs) and [platform metrics](https://docs.microsoft.com/azure/iot-hub/monitor-iot-hub-reference#metrics), available through Azure Monitor.  

We're aware of a bug on metrics export (via the AllMetrics category) with connectedDeviceCount and totalDeviceCount metrics and certain aggregation types. Workaround: [metrics alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric) are unaffected by the bug, and the "Total" aggregation type in the export is also unaffected. 

 

## **Recommended Documents** 

 

* [Azure Monitor overview](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview)