<properties
	pageTitle="IoT Hub direct method issues"
	description="IoT Hub direct method issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
  	ms.author="jlian,saziz,jtanner"
	displayOrder="85"
	selfHelpType="resource"
	supportTopicIds="32630547"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax, usnat, ussec"
	articleId="f9cb4e6b-59dc-4ed8-81be-f0ae0d262366"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub direct method issues  

## **Recommended Steps**

1. Try sending a direct method to the device using the [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)
1. Try sending a direct method to a different device
1. Review [operational limits](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#other-limits) and [throttling limits](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#operation-throttles) that apply to direct methods
1. If you have [logs turned on](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#direct-methods), check for common issues under the category DirectMethods:

	* **404103 DeviceNotOnline**: The device isn't reachable during the timeout period or if the device crashed/disconnected during the direct method request
	* **404001 DeviceNotFound**: The device isn't registered with IoT Hub. To fix, register the device.
	* **504101 GatewayTimeout**: The device is online, but didn't respond during the timeout period
	* **401002 AuthenticationFailed**: Either the authentication expired, or the specified device isn't found

## **Recommended Documents**

* [Configure direct method timeout (default is 30 seconds)](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods#invoke-a-direct-method-from-a-back-end-app)<br>
* [Understand and invoke direct methods from IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods#handle-a-direct-method-on-a-device)
