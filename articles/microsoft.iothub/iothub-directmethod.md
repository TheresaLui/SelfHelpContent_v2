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
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="f9cb4e6b-59dc-4ed8-81be-f0ae0d262366"
/>

# IoT Hub direct method issues  

## **Recommended Steps**

* Error 404103 DeviceNotOnline indicates that the device isn't reachable during the timeout period<br>
* Error 404001 DeviceNotFound indicates that the device isn't registered with IoT Hub<br>
* Error 504101 GatewayTimeout indicates that the device is online, but didn't respond during the timeout period<br>
* Error 401002 AuthenticationFailed indicates that either the authentication expire or the specified device isn't found.<br>
* Review [operational limits](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#other-limits) and [throttling limits](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#operation-throttles) that apply to direct methods

## **Recommended Documents**

* [Configure direct method timeout (default is 30 seconds)](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods#invoke-a-direct-method-from-a-back-end-app)<br>
* [Understand and invoke direct methods from IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods#handle-a-direct-method-on-a-device)
