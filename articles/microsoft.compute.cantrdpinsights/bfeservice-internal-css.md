<properties
pageTitle="BFE Service"
description="BFE Service not running"
infoBubbleText="Base Filtering Engine Service (BFE) is not running which may prevent RDP connectivity"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="vmhealthsignal_10f4f09d-a1e8-4536-b167-8d2573fb4f0a"
diagnosticScenario="BFE services"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>


# Base Filtering Engine Service (BFE) is not running
<!--issueDescription-->
The Base Filtering Service (BFE) service is not running. This is preventing RDP connectivity to the VM. BFE controls operation of Windows Filtering Platform (WFP) which is a network traffic processing platform. If it is not running, it prevents network connectivity to the VM.
<!--/issueDescription-->

## **Recommended Steps**
To mitigate the issue please try the below steps from [Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console)
  * Query the state of the service by executing `sc query BFE`
  * If the service is stopped, try starting the service by executing `sc start BFE`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop NSI` and start it again using `sc start BFE`
  * Once the service is started, set the service startup type to automatic by executing `sc config BFE start= auto`

In case the service is not starting due to an error or due to an issue with the depending processes, a memory dump needs to be collected to investigate further. So please reach out to us approving the memory dump collection.
