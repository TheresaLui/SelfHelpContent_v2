<properties
	pageTitle="IoT Edge failed to install or update"
	description="IoT Edge failed to install or update"
	service="microsoft.devices"
	resource="iotedge"
	authors="kgremban"
	ms.author="kgremban"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# IoT Edge failed to install or update

If IoT Edge fails during installation or update, it's often because of a missing dependency or because the installation packages don't match the device. 

## **Recommended steps**

For Linux devices:
* If you can, run `sudo iotedge check --verbose` to test for common configuration errors. 
* Make sure that the container engine is running. If you get errors trying to install the Moby container engine, [Verify your Linux kernel for Moby compatibility](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-linux#verify-your-linux-kernel-for-moby-compatibility).
* Check that you used the installation packages that match your device's operating system. There are unique packages for each [supported operating system](https://docs.microsoft.com/azure/iot-edge/support#operating-systems).

For Windows devices:
* If you can, run `iotedge check --verbose` to test for common configuration errors. 
* Verify that your device is running a [supported version of Windows](https://docs.microsoft.com/azure/iot-edge/support#operating-systems).

## **Recommended documents**

[Install the Azure IoT Edge runtime on Debian-based Linux systems](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-linux)<br>
[Install the Azure IoT Edge runtime on Windows](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge-windows)<br>
[Update the IoT Edge security daemon and runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge)