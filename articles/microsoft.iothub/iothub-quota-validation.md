<properties
	pageTitle="Quota validation issues"
	description="Quota validation issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630567"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="07984f0e-a641-4843-a804-e8015906371d"
	ownershipId="AzureIot_IotHub"
/>

# Not sure why I got throttled or ran out of quota

## **Recommended Steps**

**Common reasons for unexpectedly hitting daily quota include:**

* If you're using free (F1) edition IoT Hub, it has a smaller message meter size at 0.5 KB (as opposed to 4KB for the paid editions). This might cause you to hit daily quota sooner than expected. [Unfortunately, it's not possible to upgrade from free IoT Hub to paid](https://azure.microsoft.com/pricing/details/iot-hub/). <br>
* Typically each file upload uses two messages, one for initiation and one for completion
* Twin reads, writes, and queries are metered in 0.5-KB chunks as opposed of 4 KB

To learn more, see [IoT Hub Pricing FAQ](https://azure.microsoft.com/pricing/details/iot-hub/).

**Common questions with IoT Hub throttling include:**

* If you **didn't get 429 errors but think you've been throttled**, it might be because IoT Hub only sends 429 ThrottlingException when the limit has been violated for too long. To learn more, see [Traffic shaping](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#traffic-shaping).
* If you got **JobQuotaExceededException** with device import or export jobs, it's because you can only have one active import or export job at any point in time

To learn more, see [IoT hub throttling](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#).

## **Recommended Documents**

* [IoT Hub throttling and you](https://azure.microsoft.com/blog/iot-hub-throttling-and-you/)<br>
* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade) <br>
* [IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)<br>
* [Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
