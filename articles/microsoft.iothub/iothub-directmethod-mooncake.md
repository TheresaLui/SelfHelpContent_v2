<properties
	pageTitle="IoT Hub direct method issues"
	description="IoT Hub direct method issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
  	ms.author="jlian,saziz,jtanner"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="iothub-directmethod-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub direct method issues  

## **Recommended Steps**

1. Try sending a direct method to the device using the [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId)
2. Try sending a direct method to a different device
3. Review [operational limits](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling#other-limits) and [throttling limits](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling#operation-throttles) that apply to direct methods
4. If you have [logs turned on](https://docs.azure.cn/iot-hub/iot-hub-monitor-resource-health#direct-methods), check for common issues under the category DirectMethods:

**404103 DeviceNotOnline** 

The device isn't reachable during the timeout period or if the device crashed/disconnected during the direct method request.

**404001 DeviceNotFound** 

The device isn't registered with IoT Hub. To fix, register the device.

**504101 GatewayTimeout** 

The device is online, but didn't respond during the timeout period.

**401002 AuthenticationFailed** 

Either the authentication expired or the specified device isn't found.

## **Recommended Documents**

* [Configure direct method timeout (default is 30 seconds)](https://docs.azure.cn/iot-hub/iot-hub-devguide-direct-methods#invoke-a-direct-method-from-a-back-end-app)

* [Understand and invoke direct methods from IoT Hub](https://docs.azure.cn/iot-hub/iot-hub-devguide-direct-methods#handle-a-direct-method-on-a-device)