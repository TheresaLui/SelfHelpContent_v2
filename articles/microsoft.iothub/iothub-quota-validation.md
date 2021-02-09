<properties
  pagetitle="Not sure why I got throttled or ran out of quota&#xD;"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,saziz,jtanner"
  selfhelptype="Generic"
  supporttopicids="32630567"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="07984f0e-a641-4843-a804-e8015906371d"
  ownershipid="AzureIot_IotHub" />
# Not sure why I got throttled or ran out of quota

## **Recommended Steps**

**Common reasons for unexpectedly hitting daily quota**

If you use the free (F1) edition IoT Hub, it has a smaller message meter size (0.5 KB versus 4KB for paid editions). This can cause you to reach the daily quota sooner than expected. [Unfortunately, it's not possible to upgrade from free IoT Hub to paid](https://azure.microsoft.com/pricing/details/iot-hub/). <br>
* Typically each file upload uses two messages, one for initiation and one for completion
* Twin reads, writes, and queries are metered in 0.5 KB chunks as opposed of 4 KB

To learn more, see [IoT Hub Pricing FAQ](https://azure.microsoft.com/pricing/details/iot-hub/).

**Common questions with IoT Hub throttling**

* If you think you've been throttled but didn't get a 429 error, the cause may be because IoT Hub only sends the "429 ThrottlingException" when the limit has been violated for too long. To learn more, see [Traffic shaping](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#traffic-shaping).
* If you received a "JobQuotaExceededException" with device import or export jobs, the reason is you can only have one active import or export job at any point in time

To learn more, see [IoT Hub throttling](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#).

## **Recommended Documents**

* [IoT Hub throttling and you](https://azure.microsoft.com/blog/iot-hub-throttling-and-you/)
* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade) 
* [IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)
* [Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
