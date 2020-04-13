<properties
	pageTitle="Unable to connect downstream device after going offline"
	description="Unable to connect downstream device after going offline"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680987"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="144f0fb6-05c9-42fa-ad82-aaa48e0301fa"
	ownershipId="AzureIot_IotEdge"
/>

# My IoT Edge gateway device can't connect to downstream devices while offline

## **Recommended Steps**

If your gateway device is operating offline, verify that the downstream device is set as a child device of the gateway. You can manage the child/parent relationship from the device details page of either the IoT Edge gateway device or the downstream device. The gateway device must connect to IoT Hub once to retrieve child device information, then can operate offline. 

