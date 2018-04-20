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
Windows Firewall must be running to have connectivity to the virtual machine
<!--/issueDescription-->

## **Recommended Steps**
**Check or set Firewall Service**

Refer to the steps in the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/HowTo/Check_or_set_a_Windows_service_through_registry) that shows how to operate with the registry when connectivity to a VM is not working and change to the startup type of the service is required using registry.
