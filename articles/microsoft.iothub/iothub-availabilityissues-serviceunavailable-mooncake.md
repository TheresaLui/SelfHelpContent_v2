<properties
	pageTitle="Is IoT Hub having service issues?"
	description="Is IoT Hub having service issues?"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir"
	ms.author="jlian,saziz"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="Mooncake"
	articleId="iothub-availabilityissues-serviceunavailable-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# Is IoT Hub having service issues?

## **Recommended Steps**

1. If you're seeing 500xxx errors (i.e. 500001 ServerError), the issue is likely temporary. Make sure your device can automatically retry: [How to manage connectivity and reliable messaging using Azure IoT Hub device SDKs](https://docs.azure.cn/iot-hub/iot-hub-reliability-features-in-sdks#connection-and-retry)
2. If the issue persists, check [Azure Resource Health](data-blade:Microsoft_Azure_support.resourcehealthdetailblade) and [Azure Service Health](data-blade:hubsextension.serviceshealthblade) to see if there's a known issue on our side
3. If the issue persists, use the [manual failover feature](https://docs.azure.cn/iot-hub/tutorial-manual-failover)

## **Recommended Documents**

* [IoT Hub high availability and disaster recovery](https://docs.azure.cn/iot-hub/iot-hub-ha-dr)
* [Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.azure.cn/iot-hub/iot-hub-monitor-resource-health)
* [Azure Status](https://www.azure.cn/support/service-dashboard/)
