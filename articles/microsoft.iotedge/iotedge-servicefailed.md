<properties
  pagetitle="The iotedged service is in a failed state"
  service="microsoft.devices"
  resource="iothubs"
  ms.author="veyalla,kgremban,darobs"
  selfhelptype="Generic"
  supporttopicids="32680960"
  resourcetags=""
  productpesids="16509"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="b61692e8-5407-4199-888c-0ea3eff0402a"
  ownershipid="AzureIot_IotEdge" />
# The iotedged service is in a failed state

If the IoT Edge service is reporting a failed state, there are several possible causes, including an error in the connection string, firewall connection errors, and the container engine not running. IoT Edge has a built-in troubleshooting tool to check all these common errors at once. 

## **Recommended Steps**
Run the IoT Edge troubleshooting tool on your IoT Edge device:
 * On Linux devices: `sudo iotedge check --verbose`
 * On Windows devices: `iotedge check --verbose`

## **Recommended Documents**

* [Common issues and resolutions for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/troubleshoot)
* [Built-in troubleshooting functionality](https://github.com/Azure/iotedge/blob/master/doc/troubleshoot-checks.md)

Consider using the following channels for non-blocking incidents: 
* Prior issues at [azure/iotedge GitHub repository](https://github.com/azure/iotedge/issues?q=is%3Aissue+)  
    * Issues in the repo are monitored by the IoT Edge product team  
* Stack Overflow questions tagged [azure-iot-edge](https://stackoverflow.com/questions/tagged/azure-iot-edge)  
* [Answers for Azure Docs issues](https://github.com/MicrosoftDocs/azure-docs/issues?q=is%3Aissue+label%3Aiot-edge%2Fsvc+) 
* [IoT Edge Q&A portal](https://docs.microsoft.com/answers/topics/azure-iot-edge.html?WT.mc_id=Portal-Microsoft_Azure_Support)
