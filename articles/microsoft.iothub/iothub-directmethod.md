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
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="f9cb4e6b-59dc-4ed8-81be-f0ae0d262366"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub direct method issues  

## **Recommended Steps**

1. Try sending a direct method to the device using the [IoT Devices tab](data-blade:Microsoft_Azure_IotHub.DeviceExplorerBlade.id.$resourceId) or [CLI](https://github.com/azure/azure-iot-cli-extension).
1. Try sending a direct method to a different device
1. Review [operational limits](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#other-limits) and [throttling limits](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#operation-throttles) that apply to direct methods
1. If you have [logs turned on](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health#direct-methods), check for common issues under the category DirectMethods:

* [404103 DeviceNotOnline](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-404103-devicenotonline)
* [404001 DeviceNotFound](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-404001-devicenotfound)
* [504101 GatewayTimeout](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-504101-gatewaytimeout)
* [401003 IoTHubUnauthorized](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-error-401003-iothubunauthorized)

## **Recommended Documents**

* [Configure direct method timeout (default is 30 seconds)](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods#invoke-a-direct-method-from-a-back-end-app)<br>
* [Understand and invoke direct methods from IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods#handle-a-direct-method-on-a-device)
