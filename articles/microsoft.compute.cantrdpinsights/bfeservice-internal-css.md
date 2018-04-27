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


# Base Filtering Engine (BFE) Service is not running
<!--issueDescription-->
The Base Filtering Service (BFE) service is not running on your virtual machine. This is preventing RDP connectivity to the VM.  The BFE service controls the operation of the Windows Filtering Platform (WFP) which is a network traffic processing platform. If it is not running, network connectivity to the VM will not function correctly.
<!--/issueDescription-->

## **Recommended Steps**
To resolve the issue, please try the steps below using the Azure virtual machine serial console tool.  If you’re unfamiliar with the serial console or would like additional information, please refer to our user [guide] (https://docs.microsoft.com/azure/virtual-machines/windows/serial-console).   
  * Query the state of the service by executing `sc query BFE`
  * If the service is stopped, try starting the service by executing `sc start BFE`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop NSI` and start it again using `sc start BFE`
  * Once the service is started, set the service startup type to automatic by executing `sc config BFE start= auto`

If the service is not starting due to an error or an issue with dependent processes, a memory dump needs to be collected to continue troubleshooting. If this is the case for you, please email us with your approval to collect a memory dump of this VM and we will investigate further.  
