<properties
	pageTitle="IoT Hub file upload issues"
	description="IoT Hub file upload issues"
	service="microsoft.devices"
	resource="iothubs"
	authors="jlian,meetshamir,jtanner-msft"
  	ms.author="jlian,saziz,jtanner"
	displayOrder="55"
	selfHelpType="resource"
	supportTopicIds="32630550"
	resourceTags=""
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="e8c8696f-8eb2-4cc0-9ef8-0269133edfc0"
/>

# IoT Hub file upload issues

## **Recommended Steps**

1. If the initital file upload operation fails, please retry
2. If the problem still persists, check the device client logs to see if there is an error related to file upload limits similar to "Error Code: 403006 - Number of active file upload requests exceeded limit"
3. Note that each device client is limited to [10 cuncurrent file uploads](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#other-limits)
4. If you are hitting that limit, [verify the previous uploads are completed](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload#notify-iot-hub-of-a-completed-file-upload)

## **Recommended Documents**

* [Upload files with IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload)<br>
* [Configure IoT Hub file uploads using the Azure portal](https://docs.microsoft.com/azure/iot-hub/iot-hub-configure-file-upload)
