<properties
  pagetitle="Connection Timeout issues&#xD;"
  description="Connection Timeout issues"
  service="microsoft.devices"
  resource="iotsdks"
  ms.author="elhorton"
  selfhelptype="Generic"
  supporttopicids="32596694"
  resourcetags=""
  productpesids="16122"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="055ca67b-dcf8-4f17-99f8-a39a629217f8"
  ownershipid="AzureIot_IotHub" />
# Connection Timeout issues

## **Recommended documents**
[Reliability features in the device SDK](https://docs.microsoft.com/azure/iot-hub/iot-hub-reliability-features-in-sdks)<br>
[Protocol FAQs](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-protocols)<br>
[Diagnosing connectivity using iothub-diagnostics](https://github.com/Azure/iothub-diagnostics)<br>
[Monitor the health of Azure IoT Hub and diagnose problems quickly](https://docs.microsoft.com/azure/iot-hub/iot-hub-monitor-resource-health)

## **Notes**
Ensure that each device has its own device identity-- do not share device connection strings across multiple devices. They will fight for the same connection.

Ensure that you are only using one device client per device application. Similar to the scenario above, multiple device clients with the same connection details will contend for the same connection, causing frequent timeouts and reconnects. 

For a more detailed explanation, see [this example in the Python SDK](https://github.com/Azure/azure-iot-sdk-python/wiki/pitfalls#its-easy-to-create-multiple-client-instances-and-cause-instability)