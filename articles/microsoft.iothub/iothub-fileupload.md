<properties
  pagetitle="IoT Hub file upload issues&#xD;"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="jlian,saziz,jtanner,yiygu"
  selfhelptype="Resource"
  supporttopicids="32630550"
  resourcetags=""
  productpesids="15946"
  cloudenvironments="public,blackforest,fairfax,usnat,ussec,mooncake"
  articleid="e8c8696f-8eb2-4cc0-9ef8-0269133edfc0"
  ownershipid="AzureIot_IotHub" />
# IoT Hub file upload issues

## **Recommended Steps**

1. If the initial file upload operation fails, please retry
1. If you see "Error Code: 403006 - Number of active file upload requests exceeded limit", note that each device client is limited to [10 concurrent file uploads](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-quotas-throttling#other-limits)
1. If you reached the aforementioned limit, [verify the previous uploads are completed](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload#notify-iot-hub-of-a-completed-file-upload)

## **Recommended Documents**

* [Upload files with IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-file-upload)
* [Configure IoT Hub file uploads using the Azure portal](https://docs.microsoft.com/azure/iot-hub/iot-hub-configure-file-upload)
