<properties
pageTitle="VM Health Signal"
description="Firewall Misconfigured"
infoBubbleText="Firewall Misconfigured"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_4d7f5e70-4f1d-48b0-aadd-6bf8e36f3d4a"
diagnosticScenario="Firewall Misconfigured"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# Guest VM Health Signal Insight
<!--issueDescription-->
## **Firewall is set to block all inbound connections**
Following three scenarios could trigger this:

1. The RDP rule is not setup to allow the RDP traffic
2. Guest OS firewall profiles were setup to block all inbound connections and this includes the RDP traffic
3. The machine is having an AD policy that is blocking every connection that is not from one specific network subset and from SAW devices
<!--/issueDescription-->

## **Recommended Steps - Internal**
**Use Custom Script Extension or backup OS disk and set up the Troubleshooting environment**

Please note, if the Guest OS is not allowing traffic, Custom Script Extension will not work since it uses the network stack so there's no way to get to the VM so you need to work on the machine directly in OFFLINE mode

Please refer to the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/TSG/Isolation_Bucket/GuestOS_firewall_blocking_inbound_traffic) to RCA and view mitigation steps in detail.

Mitigations based on RCA:

1. Enable-Disable a Firewall rule on a Guest OS
2. Attach the OS disk to a troubleshooting VM where you can perform the changes locally on the registry
3. Check registries to validate the scenario (this is a common case on Nebula cases, MSIT cases or for internal customer in general)
