<properties
  pagetitle="Messages aren't being routed between modules or not being received"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="darobs"
  selfhelptype="Generic"
  supporttopicids="32680971,32680972"
  resourcetags=""
  productpesids="16509"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="69fb242f-5690-44f4-9426-e3a2923a974d"
  ownershipid="AzureIot_IotEdge" />
# Messages aren't being routed between modules or not being received

IoT Edge uses routing to connect message inputs and outputs of individual modules so that you can create communication pipelines in your deployments. Use these steps to troubleshoot. 

## **Recommended Steps**

* Turn on debug logs for the IoT Edge hub to see if you're getting **sent** and **received** confirmations for each module. For more information, 

	* _1.1 (and earlier)_ See [View the messages going through the IoT Edge hub](https://docs.microsoft.com/azure/iot-edge/troubleshoot?view=iotedge-2018-06#view-the-messages-going-through-the-iot-edge-hub).
	* _1.2 (and later)_ See [View the messages going through the IoT Edge hub](https://docs.microsoft.com/azure/iot-edge/troubleshoot?view=iotedge-2020-11#view-the-messages-going-through-the-iot-edge-hub).

* Inspect each of the modules to see if they're successfully sending messages
* Double check the routes in your deployment manifest. Pay particular attention to the following common errors:

	* Do the names of the modules in your route match the actual names of the modules running on your device? Names are case sensitive.
	* Does each named input and output exist in the correct module?

* Update to the latest IoT Edge Runtime:

	* _1.1 (and earlier)_ See [how to upgrade the IoT Edge runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2018-06&WT.mc_id=Portal-Microsoft_Azure_Support).
	* _1.2 (and later)_ See [how to upgrade the IoT Edge runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2020-11&WT.mc_id=Portal-Microsoft_Azure_Support).

## **Recommended Documents**

**1.1 (and earlier)**

* [Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot?view=iotedge-2018-06)
* [Learn how to deploy modules and establish routes in IoT Edge](https://docs.microsoft.com/azure/iot-edge/module-composition?view=iotedge-2018-06)

**1.2 (and later)**

* [Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot?view=iotedge-2020-11)
* [Learn how to deploy modules and establish routes in IoT Edge](https://docs.microsoft.com/azure/iot-edge/module-composition?view=iotedge-2020-11)
