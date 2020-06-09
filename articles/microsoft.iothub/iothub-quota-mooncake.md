<properties
	pageTitle="Manage your IoT Hub pricing or scale"
	description="Manage your IoT Hub pricing or scale"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder="17"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="iothub-quota-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# Manage your IoT Hub pricing or scale

## **Recommended Steps**

1. To upgrade IoT hub to a higher tier, go to [Pricing and scale](data-blade:Microsoft_Azure_IotHub.IotHubPricingAndScaleBlade.id.$resourceId), and [choose a tier](https://docs.azure.cn/zh-cn/iot-hub/iot-hub-scaling)
2. It is [not currently possible](https://www.azure.cn/pricing/details/iot-hub/) to upgrade from IoT Hub free edition (F1) to one of the paid editions. For a workaround, use [ARM templates](https://docs.azure.cn/azure-resource-manager/manage-resources-powershell) to create a paid IoT hub with the same settings, and import device identities from the free IoT hub with our [bulk device management API](https://docs.azure.cn/iot-hub/iot-hub-bulk-identity-mgmt).
3. For other types of quota increases, like maximum units, number of hubs in a subscription, or maximum device count, please open a support request.

## **Recommended Documents**

* [How to upgrade your IoT hub](https://docs.azure.cn/iot-hub/iot-hub-upgrade)
* [IoT hub pricing examples](https://docs.azure.cn/iot-hub/iot-hub-devguide-pricing)
* [IoT Hub pricing](https://www.azure.cn/pricing/details/iot-hub/)
