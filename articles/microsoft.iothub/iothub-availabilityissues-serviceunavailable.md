<properties
	pageTitle="Is IoT Hub having service issues?"
	description="Is IoT Hub having service issues?"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir"
	ms.author="jlian,saziz"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32630528"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax, usnat, ussec"
	articleId="5b98dc45-7683-4608-8213-61669651e6ef"
	ownershipId="AzureIot_IotHub"
/>

# Is IoT Hub having service issues?

## **Recommended Steps**

1. If you're seeing 500xxx errors (i.e. 500001 ServerError), the issue is likely temporary. Make sure your device can automatically retry: [How to manage connectivity and reliable messaging using Azure IoT Hub device SDKs](https://docs.microsoft.com/azure/iot-hub/iot-hub-reliability-features-in-sdks#connection-and-retry)
2. If the issue persists, check [Azure Resource Health](data-blade:Microsoft_Azure_Health.ResourceHealthDetailBlade.resourceId.$resourceId) and [Azure Service Health](data-blade:Microsoft_Azure_Health.ServiceIssuesBlade) to see if there's a known issue on our side
3. If the issue persists, consider [a manual failover of your IoT Hub to the geo-paired region](https://docs.microsoft.com/azure/iot-hub/tutorial-manual-failover)

## **Recommended Documents**

* [IoT Hub high availability and disaster recovery](https://docs.microsoft.com/azure/iot-hub/iot-hub-ha-dr)<br>
* [Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health)<br>
* [Azure Status](https://azure.microsoft.com/status)
