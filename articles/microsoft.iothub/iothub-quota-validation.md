<properties
	pageTitle="Quota validation issues"
	description="Quota validation issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
 	ms.author="jlian,saziz,jtanner"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596659,32630567"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="07984f0e-a641-4843-a804-e8015906371d"
/>

# Not sure why I got throttled or ran out of quota

## **Recommended Steps**

1. Review [Understand IoT Hub quota and throttling](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling)
1. If you're using free (F1) edition IoT Hub, it has a smaller chunking limit at 0.5KB (as opposed to 4KB for the paid editions). This might cause you to hit daily quota sooner than expected.
1. [Unfortunately, it's not possible to upgrade from free IoT Hub to paid](https://azure.microsoft.com/pricing/details/iot-hub/). 

## **Recommended Documents**

* [IoT Hub throttling and you](https://azure.microsoft.com/blog/iot-hub-throttling-and-you/)<br>
* [How to upgrade your IoT hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-upgrade) <br>
* [IoT Hub pricing](https://azure.microsoft.com/pricing/details/iot-hub/)<br>
* [Choose the right IoT Hub tier for your solution](https://docs.microsoft.com/azure/iot-hub/iot-hub-scaling)
