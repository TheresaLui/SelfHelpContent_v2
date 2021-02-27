<properties
	pageTitle="IoT Edge failed to install or update on Windows"
	description="IoT Edge failed to install or update on Windows"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban,micahl"
	ms.author="veyalla,kgremban,micahl"
	selfHelpType="generic"
	supportTopicIds="32784220"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="8a8a9667-f45c-47b8-bcf5-30869f17e155"
	ownershipId="AzureIot_IotEdge"
/>

# IoT Edge failed to install or update on Windows

If IoT Edge fails during installation or update, it's often because of a missing dependency or because the installation packages don't match the device. 

## **Recommended Steps**

1. If you can, run the command **iotedge check --verbose** to test for common configuration errors
2. Verify that your device is running a [supported version of Windows](https://docs.microsoft.com/azure/iot-edge/support?view=iotedge-2018-06#operating-systems). Windows 10 Enterprise is not supported to host IoT Edge due to licensing issues. The EULA explicitly excludes the use of Windows Containers on non-Server and non-IOT editions of Windows in product environments.

## **Recommended Documents**

* [Install the Azure IoT Edge runtime on Windows](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-windows?view=iotedge-2018-06)
* [Install and provision Azure IoT Edge for Linux on a Windows device](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-on-windows?view=iotedge-2018-06)

