<properties
	pageTitle="After installation, the IoT Edge agent doesn't start"
	description="After installation, the IoT Edge agent doesn't start"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680959"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="71f4073c-11e9-4448-8f14-dcf64a098fdb"
/>

# After installation, the IoT Edge agent doesn't start

When you install or update Azure IoT Edge, or even when an IoT Edge device restarts, the IoT Edge agent module should start automatically. This process may take some time on smaller devices or in areas with slow connections, because the agent module image is large. Use the recommended steps to troubleshoot whether the image is starting slowly, or whether there's an error to resolve. 

## **Recommended steps**

1. Run the IoT Edge troubleshooting tool on your IoT Edge device to check for common configuration or connectivity issues.

  * On Linux devices: `sudo iotedge check --verbose`
  * On Windows devices: `iotedge check --verbose`

2. View the logs of the IoT Edge security manager, which should tell you whether the image download is still in progress or failed.

  * On Linux devices: `sudo journalctl -u iotedge -f`
  * On Windows devices: `. {Invoke-WebRequest -useb https://aka.ms/iotedge-win} | Invoke-Expression; Get-IoTEdgeLog`

3. Restart the IoT Edge service.

  * On Linux devices: `sudo systemctl restart iotedge`
  * On Windows devices: `Stop-Service iotedge` and `Start-Service iotedge`

## **Recommended documents**

[Built-in troubleshooting functionality](https://github.com/Azure/iotedge/blob/master/doc/troubleshoot-checks.md)