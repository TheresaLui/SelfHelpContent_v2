<properties
	pageTitle="IoT Hub file upload issues"
	description="IoT Hub file upload issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
  	ms.author="jlian,saziz,jtanner"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="iothub-fileupload-mooncake"
	ownershipId="AzureIot_IotHub"
/>

# IoT Hub file upload issues

## **Recommended Steps**

1. If the initial file upload operation fails, please retry
2. If you see **Error Code: 403006 - Number of active file upload requests exceeded limit**, note that each device client is limited to [10 concurrent file uploads](https://docs.azure.cn/iot-hub/iot-hub-devguide-quotas-throttling#other-limits)
3. If you are hitting that limit, [verify the previous uploads are completed](https://docs.azure.cn/iot-hub/iot-hub-devguide-file-upload#notify-iot-hub-of-a-completed-file-upload)

## **Recommended Documents**

* [Upload files with IoT Hub](https://docs.azure.cn/iot-hub/iot-hub-devguide-file-upload)
* [Configure IoT Hub file uploads using the Azure portal](https://docs.azure.cn/iot-hub/iot-hub-configure-file-upload)
