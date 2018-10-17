<properties
pageTitle="Netlogon service Not running"
description="NetlogonNotRunning"
infoBubbleText="Netlogon service is not running in your VM preventing network connectivity. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="NetlogonService"
diagnosticScenario="Netlogon service Not running"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# Netlogon Service is not running

<!--issueDescription-->
The Netlogon service is not running on the virtual machine, causing a loss of network connectivity. This could happen if the service is disabled accidentally or if the service is crashing or hung.

<!--/issueDescription-->

## **Recommended Steps**
To resolve the issue, please try the steps below using the Azure virtual machine serial console.  If you’re unfamiliar with the serial console or would like additional information, please refer to our user [guide](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console).

#### From the console: ####
  * Query the state of the service by executing `sc query Netlogon`
  * If the service is stopped, try starting the service by executing `sc start Netlogon`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop Netlogon` and start it again using `sc start Netlogon`
  * Once the service is started, set the service startup type to automatic by executing `sc config Netlogon start= auto`

If the service is not starting due to an error or an issue with dependent processes, a memory dump needs to be collected to continue troubleshooting. If this is the case for you, please email us with your approval to collect a memory dump of this VM and we will investigate further.
