<properties
pageTitle="VM Health Signal"
description="Terminal Service"
infoBubbleText="Terminal Service"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_4c4d26e0-293f-435b-83fe-3ac0169d6cdf"
diagnosticScenario="Administrator Setting"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# Guest VM Health Signal Insight
<!--issueDescription-->
## **Terminal Service is not running**
Terminal Service is not running and hence RDP connectivity is impacted
<!--/issueDescription-->

## **Recommended Steps - Internal**
**Check or set Terminal Service**

Refer to the steps in the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/HowTo/Check_or_set_a_Windows_service_through_registry) that shows how to operate with the registry when connectivity to a VM is not working and change to the startup type of the service is required using registry.
