<properties
pageTitle="NSI service Not running"
description="NSINotRunning"
infoBubbleText="Network Store Interface Service (NSI) is not running"
service="microsoft.compute"
resource="virtualmachines"
authors="ramakk"
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

* From [Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console) `sc query NSI`
  * If the service is stopped, try starting the service `sc start NSI`
  * If the service is hung at starting to stopping try stopping the service `sc stop NSI` and try starting the service.
  * If you the service is still hung, collect [procdump](https://docs.microsoft.com/sysinternals/downloads/procdump) to investigate further. Detailed process can be found in the internal article.
  * In case the service is not starting due to an error or due to an issue with the depending processes, collect a memory dump to debug the issue.
* Set the service status to auto start type using `sc config NSI start= auto`




<!--/issueDescription-->

## **Recommended Steps**
**Check or set NSI Service**

Refer to the steps in the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/CantRDPSSH/TSG/Isolation_Bucket/Network_Store_Interface_service_is_not_starting) for detailed troubleshooting steps.
