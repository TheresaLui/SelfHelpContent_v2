<properties
  pagetitle="Not sure why I got throttled or ran out of quota&#xD;"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,saziz,jtanner,yiygu"
  selfhelptype="Generic"
  supporttopicids="32630557,32630561"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="07984f0e-a641-4843-a804-e8015906371d"
  ownershipid="AzureIot_IotHub" />
# Not sure why I got throttled or ran out of quota

## **Recommended Steps**

**Common reasons for unexpectedly hitting daily quota**

This can be resolved by adding units to the IoT Hub or upgrading its SKU level.

If you use the free (F1) edition IoT Hub, it has a smaller message meter size (0.5 KB versus 4KB for paid editions). This can cause you to reach the daily quota sooner than expected. [Unfortunately, it's not possible to upgrade from free IoT Hub to paid](https://azure.microsoft.com/pricing/details/iot-hub/). <br>
* Typically each file upload uses two messages, one for initiation and one for completion

To learn more, see [IoT Hub Pricing FAQ](https://azure.microsoft.com/pricing/details/iot-hub/).

## **Recommended Documents**

* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade) 
* [IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)
* [Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)