<properties
pageTitle="NSI service Not running"
description="NSINotRunning"
infoBubbleText="Network Store Interface Service (NSI) is not running"
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="NSIService"
diagnosticScenario="NSI service Not running"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# Network Store Interface Service (NSI) is not running

<!--issueDescription-->
The NSI service is not running on the Virtual Machine. This impacts the network connectivity of the VM. This could happen if the service is disabled accidentally or if the service is crashing or hung.
<!--/issueDescription-->

## **Recommended Steps**
To mitigate the issue please try the below steps from [Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console)
  * Query the state of the service by executing `sc query NSI`
  * If the service is stopped, try starting the service by executing `sc start NSI`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop NSI` and start it again using `sc start NSI`
  * Once the service is started, set the service startup type to automatic by executing `sc config NSI start= auto`

In case the service is not starting due to an error or due to an issue with the depending processes, a memory dump needs to be collected to investigate further. So please reach out to us approving the memory dump collection.
