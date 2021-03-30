<properties
  pagetitle="Manage your IoT Hub pricing or scale&#xD;"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,saziz,jtanner"
  selfhelptype="Resource"
  supporttopicids="32630557,32630561"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="6a85270e-9f76-4a77-bdba-79c38d4a5461"
  ownershipid="AzureIot_IotHub" />
# Manage your IoT Hub pricing or scale

## **Recommended Steps**

1. To upgrade IoT hub to a higher tier, go to [**Pricing and scale**](data-blade:Microsoft_Azure_IotHub.IotHubPricingAndScaleBlade.id.$resourceId), and [choose a tier](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
1. Upgrading from the IoT Hub free edition (F1) to a paid edition is [not currently possible](https://azure.microsoft.com/pricing/details/iot-hub/). As a workaround, use [ARM templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-export-template-powershell) to create a paid IoT hub with the same settings, and import device identities from the free IoT hub with our [bulk device management API](https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt).
1. For all other types of quota increases, such as maximum units, number of hubs in a subscription, or maximum device count, open a support request

## **Recommended Documents**

* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade)
* [IoT hub pricing examples](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-pricing)
* [IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)
