<properties
  pagetitle="My IoT Edge device doesn't reconnect after coming back online"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="veyalla,kgremban,darobs"
  selfhelptype="Generic"
  supporttopicids="32680983"
  resourcetags=""
  productpesids="16509"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="ff4317fd-3c49-446d-882b-bef72440ed17"
  ownershipid="AzureIot_IotEdge" />
# My IoT Edge device doesn't reconnect after coming back online

Azure IoT Edge is designed to operate while offline, and then automatically reconnect to IoT Hub when it's online. If your IoT Edge device doesn't reconnect, follow these steps to resolve the problem.

## **Recommended Steps**

* Give the device sufficient time to reconnect. On some platforms, it may take up to 10 minutes. 
* Check the version of IoT Edge on your device by running the command `iotedge --version`. Update your device to version 1.0.7-1 or newer to take advantage of an SDK fix for intermittent connectivity issues.
* Use the built-in troubleshooting tool on the IoT Edge device to check for common connection errors:
  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`

## **Recommended Documents**

* [Update the IoT Edge security daemon and runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge)

In addition, considering using the following channels for non-blocking incidents: 
* Prior issues at [azure/iotedge GitHub repository](https://github.com/azure/iotedge/issues?q=is%3Aissue+)  
    * Issues in the repo are monitored by the IoT Edge product team  
* Stack Overflow questions tagged [azure-iot-edge](https://stackoverflow.com/questions/tagged/azure-iot-edge)  
* [Answers to Azure Docs issues](https://github.com/MicrosoftDocs/azure-docs/issues?q=is%3Aissue+label%3Aiot-edge%2Fsvc+) 
* [IoT Edge Q&A portal](https://docs.microsoft.com/answers/topics/azure-iot-edge.html?WT.mc_id=Portal-Microsoft_Azure_Support)
