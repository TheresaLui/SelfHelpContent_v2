<properties
  pagetitle="My IoT Edge gateway device can't connect to downstream devices while offline"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="darobs"
  selfhelptype="Generic"
  supporttopicids="32680987"
  resourcetags=""
  productpesids="16509"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="144f0fb6-05c9-42fa-ad82-aaa48e0301fa"
  ownershipid="AzureIot_IotEdge" />
# My IoT Edge gateway device can't connect to downstream devices while offline

## **Recommended Steps**

If your gateway device is operating offline, verify that the downstream device is set as a child device of the gateway. You can manage the child/parent relationship from the device details page of either the IoT Edge gateway device or the downstream device. The gateway device must connect to IoT Hub once to retrieve child device information, then can operate offline.

## **Recommended Documents**

* [Understand extended offline capabilities for IoT Edge devices, modules, and child devices.](https://docs.microsoft.com/azure/iot-edge/offline-capabilities)
