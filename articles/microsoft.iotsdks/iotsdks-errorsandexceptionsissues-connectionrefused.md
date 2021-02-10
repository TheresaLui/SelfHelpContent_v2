<properties
  pagetitle="Connection refuse issues"
  description="Connection refuse issues"
  service="microsoft.devices"
  resource="iotsdks"
  ms.author="elhorton"
  selfhelptype="Generic"
  supporttopicids="32596693"
  resourcetags=""
  productpesids="16122"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="90f077ba-08a5-45ba-a4ae-37c8c13f37ac"
  ownershipid="AzureIot_IotHub" />
# Connection refuse issues

## **Recommended documents**
[Detect and troubleshoot disconnects](https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-connectivity)<br>
[IoT Hub SDK reference](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-sdks)<br>
[Reliability features in the device SDK](https://docs.microsoft.com/azure/iot-hub/iot-hub-reliability-features-in-sdks)

**Notes**

Ensure that each device has its own device identity-- do not share device connection strings across multiple devices. They will fight for the same connection.

Ensure that you are only using one device client per device application. Similar to the scenario above, multiple device clients with the same connection details will contend for the same connection, causing frequent timeouts and reconnects. 

For a more detailed explanation, see [this example in the Python SDK](https://github.com/Azure/azure-iot-sdk-python/wiki/pitfalls#its-easy-to-create-multiple-client-instances-and-cause-instability)