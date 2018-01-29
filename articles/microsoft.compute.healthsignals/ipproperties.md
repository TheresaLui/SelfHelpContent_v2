<properties
pageTitle="VM Health Signal"
description="Network Adapters"
infoBubbleText="IP Properties"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_6a64eeb8-eb00-4d88-a24e-e577533724b9"
diagnosticScenario="IP Properties Error"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# Guest VM Health Signal Insight
<!--issueDescription-->
## **Static IP is set at the guest OS level**
The virtual machine seems to have disabled DHCP disabled and IP address not equal to null. This indicates static IP is set at the Guest OS level.
<!--/issueDescription-->

## **Recommended Steps**
**Reset NIC**

Please refer to steps on how to reset NIC in the public article: <br> https://docs.microsoft.com/en-us/azure/virtual-machines/windows/reset-network-interface
