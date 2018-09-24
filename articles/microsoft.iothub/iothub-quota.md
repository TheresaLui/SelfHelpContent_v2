<properties
	pageTitle="I want to upgrade IoT Hub or increase my quota"
	description="I want to upgrade IoT Hub or increase my quota"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32596642,32596611,32596660"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# I want to upgrade IoT Hub or increase my quota

## **Recommended steps**

1. To upgrade IoT hub to a higher tier, go to [Pricing and scale](data-blade:Microsoft_Azure_IotHub.IotHubPricingAndScaleBlade.Id.$resourceId), and choose a tier. <br>
[Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)

1. If you're looking to upgrade from IoT Hub free edition (F1) to one of the paid editions, it's [unfortunately not possible](https://azure.microsoft.com/pricing/details/iot-hub/). For a workaround, use ARM templates to create a paid IoT hub with the same settings, and import device identities from the free IoT hub with our bulk device management API.<br>
[Export a resource group as ARM template](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-export-template-powershell)<br>
[IoT Hub bulk device management](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt)

1. For other types of quota increases, like maximum units, number of hubs in a subscription, or maximum device count, proceed to open a support request.

## **Recommended documents**
[How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade)<br>
[IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)<br>
