<properties
	pageTitle="IoT Edge failed to install or update on Linux"
	description="IoT Edge failed to install or update on Linux"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban,micahl"
	ms.author="veyalla,kgremban,micahl"
	selfHelpType="generic"
	supportTopicIds="32784219"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="3378f6d4-5bb5-43b2-8d8e-a3fbb5293b11"
	ownershipId="AzureIot_IotEdge"
/>

# IoT Edge failed to install or update on Linux

If IoT Edge fails during installation or update, it's often because of a missing dependency or because the installation packages don't match the device. 

## **Recommended Steps**

**IoT Edge 1.1 (and earlier)**

1. If you can, run the command **sudo iotedge check --verbose** to test for common configuration errors
2. Make sure that the container engine is running. If you get errors trying to install the Moby container engine [verify your Linux kernel for Moby compatibility](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge?view=iotedge-2018-06#install-a-container-engine).
3. Check that you used the installation packages that match your device's operating system. There are unique packages for each [supported operating system](https://docs.microsoft.com/azure/iot-edge/support#operating-systems?view=iotedge-2018-06).

**IoT Edge 1.2 (and later)**

1. If you can, run the command **sudo iotedge check --verbose** to test for common configuration errors
2. Make sure that the container engine is running. If you get errors trying to install the Moby container engine [verify your Linux kernel for Moby compatibility](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge?view=iotedge-2020-11#install-a-container-engine).
3. Check that you used the installation packages that match your device's operating system. There are unique packages for each [supported operating system](https://docs.microsoft.com/azure/iot-edge/support?view=iotedge-2020-11#operating-systems).

## **Recommended Documents**

**1.1 (and earlier)**

* [Install the Azure IoT Edge runtime on Debian-based Linux systems](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-linux?view=iotedge-2018-06)
* [How to Update IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2018-06)

**1.2 (and later)**

* [Install the Azure IoT Edge runtime on Debian-based Linux systems](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-linux?view=iotedge-2020-11)
* [How to Update IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2020-11)

