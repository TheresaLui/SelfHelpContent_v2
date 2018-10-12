<properties
	pageTitle="Is IoT Hub having service issues?"
	description="Is IoT Hub having service issues?"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32596602,32596665,32596657"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# Is IoT Hub having service issues?

## **Recommended steps**

1. If you're seeing 500xxx errors (500001 ServerError), the issue is likely temporary. Make sure your device can automatically retry.<br>
[How to manage connectivity and reliable messaging using Azure IoT Hub device SDKs](https://docs.microsoft.com/azure/iot-hub/iot-hub-reliability-features-in-sdks#connection-and-retry)

1. If the issue persists, check [Azure Resource Health](data-blade:Microsoft_Azure_support.resourcehealthdetailblade) and [Azure Service Health](data-blade:hubsextension.serviceshealthblade) to see if there's a known issue on our side.

## **Recommended documents**
[IoT Hub high availability and disaster recovery](https://docs.microsoft.com/azure/iot-hub/iot-hub-ha-dr)<br>
[Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health)