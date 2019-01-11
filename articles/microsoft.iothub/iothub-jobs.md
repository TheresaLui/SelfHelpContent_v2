<properties
	pageTitle="IoT Hub job issues"
	description="IoT Hub job issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
  	ms.author="jlian,saziz,jtanner"
	displayOrder="65"
	selfHelpType="resource"
	supportTopicIds="32630555"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# IoT Hub job issues

## **Recommended steps**
1. There are limitations on the [number of cuncurrent jobs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#other-limits) that can be run based on the SKU of IoT Hub. 

1. There are also throttles on the [number of job operations and job device operations](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#operation-throttles) that can happen per second.

1. You can only have one active device import/export job at a time.


## **Recommended documents**
[IoT Hub quotas and throttling](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)<br>
[Schedule jobs on multiple devices](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-jobs)<br>
[Manage your IoT Hub device identities in bulk](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt)
