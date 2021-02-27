<properties
	pageTitle="IoT Edge failed to install or update"
	description="IoT Edge failed to install or update"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680942"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="243b558c-cc75-4000-afba-f0e0f3f6c818"
	ownershipId="AzureIot_IotEdge"
/>

# IoT Edge failed to install or update

If IoT Edge fails during installation or update, it's often because of a missing dependency or because the installation packages don't match the device. 

## **Recommended Steps**

**1.1 (and earlier)**

For Linux devices:<br>

1. If you can, run the command **sudo iotedge check --verbose** to test for common configuration errors
2. Make sure that the container engine is running. If you get errors trying to [install the Moby container engine](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge?view=iotedge-2018-06#install-a-container-engine).
3. Check that you used the installation packages that match your device's operating system. There are unique packages for each [supported operating system](https://docs.microsoft.com/azure/iot-edge/support#operating-systems?view=iotedge-2018-06).

For Windows devices:<br>

1. If you can, run the command **iotedge check --verbose** to test for common configuration errors
2. Verify that your device is running a [supported version of Windows](https://docs.microsoft.com/azure/iot-edge/support?view=iotedge-2018-06#operating-systems). Windows 10 Enterprise is not supported to host IoT Edge due to licensing issues. The EULA explicitly excludes the use of Windows Containers on non-Server and non-IOT editions of Windows in product environments.

**1.2 (and later)**

For Linux devices:<br>

1. If you can, run the command **sudo iotedge check --verbose** to test for common configuration errors
2. Make sure that the container engine is running. If you get errors trying to [install the Moby container engine](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge?view=iotedge-2020-11#install-a-container-engine).
3. Check that you used the installation packages that match your device's operating system. There are unique packages for each [supported operating system](https://docs.microsoft.com/azure/iot-edge/support?view=iotedge-2020-11#operating-systems).

For Windows devices:<br>

__Pending support for v1.2 in Edge for Linux on Windows (EFLOW)__

## **Recommended Documents**

**1.1 (and earlier)**

* [Install the Azure IoT Edge runtime on Debian-based Linux systems](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-linux?view=iotedge-2018-06)
* [Install the Azure IoT Edge runtime on Windows](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-windows?view=iotedge-2018-06)
* [How to Update IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2018-06)

**1.2 (and later)**

* [Install the Azure IoT Edge runtime on Debian-based Linux systems](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-linux?view=iotedge-2020-11)
* [Install the Azure IoT Edge runtime on Windows](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-windows?view=iotedge-2020-11)
* [How to Update IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?view=iotedge-2020-11)

