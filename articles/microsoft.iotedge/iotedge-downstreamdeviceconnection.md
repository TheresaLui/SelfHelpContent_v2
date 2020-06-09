<properties
	pageTitle="Downstream device can't connect to an IoT Edge gateway"
	description="Downstream device can't connect to an IoT Edge gateway"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680979"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="73d78d4d-24a5-40e9-b7d3-a5158975e098"
	ownershipId="AzureIot_IotEdge"
/>

# Downstream device can't connect to an IoT Edge gateway

For a downstream device to connect to an IoT Edge gateway, the devices need to trust each other, the downstream device needs to know how to reach the gateway, and the gateway needs to know how to authenticate the downstream device. Use the recommended steps to check that those three conditions are met. 

## **Recommended Steps**

* On the IoT Edge gateway device, run the command **iotedge check --verbose**. Look particularly at the results of the configuration checks to make sure that the certificates are valid and defined correctly
* If your gateway device is operating offline, verify that the downstream device is set as a child device of the gateway. You can manage the child/parent relationship from the device details page of either the IoT Edge gateway device or the downstream device. The gateway device must connect to IoT Hub once to retrieve child device information, then can operate offline. 
* Make sure that the downstream device and the gateway device can reach each other over your network:

  * Open communication ports on any firewalls between the two devices, and open inbound ports on the gateway device
  * Check that the gateway hostname is resolvable to an IP address. If not, use DNS or add a host file entry on the downstream device. 
  * Verify that the gateway hostname in the downstream device's connection string is the same as the hostname value in the IoT Edge config.yaml file on the gateway device

## **Recommended Documents**

* [Configure an IoT Edge device to act as a transparent gateway](https://docs.microsoft.com/azure/iot-edge/how-to-create-transparent-gateway)
* [Authenticate a downstream device to Azure IoT Hub](https://docs.microsoft.com/azure/iot-edge/how-to-authenticate-downstream-device)
* [Connect a downstream device to an Azure IoT Edge gateway](https://docs.microsoft.com/azure/iot-edge/how-to-connect-downstream-device)
