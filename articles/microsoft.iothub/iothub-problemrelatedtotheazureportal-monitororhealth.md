<properties
	pageTitle="IoT Hub logging and metrics"
	description="IoT Hub logging and metrics"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630559"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="333e2e76-151c-46ca-82b0-4dea35d409fa"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub logging and metrics

## **Recommended Steps**

1. Learn more about IoT Hub's [logging](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#understand-the-logs) and [platform metrics](https://docs.microsoft.com/azure/iot-hub/iot-hub-metrics), available through Azure Monitor. <br>
1. To use the "Logs" feature in IoT Hub, you must first [set up diagnostic logs with Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-logs-stream-log-store). This workflow typically has a 15 minutes latency.
1. We're aware of a bug on metrics export (via the AllMetrics category) with connectedDeviceCount and totalDeviceCount metrics and certain aggregation types. Workaround: [metrics alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric) are unaffected by the bug, and the "Total" aggregation type in the export is also unaffected.

## **Recommended Documents**

* [Azure Monitor overview](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview) <br>
