<properties
	pageTitle="My problem isn't listed"
	description="My problem isn't listed"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
  	ms.author="jlian,saziz,jtanner"
	displayOrder="65"
	selfHelpType="resource"
	supportTopicIds="32680883"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax, usnat, ussec"
	articleId="15dcda62-ab16-4a88-a376-3f21c390c134"
	ownershipId="AzureIot_IotHub"
/>

# My problem isn't listed

## **Recommended Steps**

* There are limitations on the [number of concurrent jobs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#other-limits) that can be run based on the SKU of IoT Hub
* There are also throttles on the [number of job operations and job device operations](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#operation-throttles) that can happen per second
* You can only have one active device import/export job at a time

## **Recommended Documents**

* [IoT Hub quotas and throttling](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)<br>
* [Schedule jobs on multiple devices](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-jobs)<br>
* [Manage your IoT Hub device identities in bulk](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt)
