<properties
pageTitle="Firewall Not running"
description="Firewall Setting"
infoBubbleText="Firewall not running"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_16f84eeb-3655-45bb-a60d-2839f159fbf4"
diagnosticScenario="Firewall Misconfigured"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# Windows Firewall is not running

<!--issueDescription-->
The Windows firewall service is not running in your virtual machine. The service must be running to enable network connectivity to the virtual machine.
<!--/issueDescription-->

## **Recommended Steps**
To mitigate the issue please try the below steps from [Serial Console](https://docs.microsoft.com/azure/virtual-machines/windows/serial-console)
  * Query the state of the service by executing `sc query Mpssvc`
  * If the service is stopped, try starting the service by executing `sc start Mpssvc`
  * If the service is hung with a status starting or stopping, try to stop the service `sc stop Mpssvc` and start it again using `sc start Mpssvc`
  * Once the service is started, set the service startup type to automatic by executing `sc config Mpssvc start= auto`

In case the service is not starting due to an error or due to an issue with the depending processes, a memory dump needs to be collected to investigate further. So please reach out to us approving the memory dump collection.
