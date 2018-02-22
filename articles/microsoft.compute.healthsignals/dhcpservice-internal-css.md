<properties
pageTitle="VM Health Signal"
description="DHCP Service not running"
infoBubbleText="DHCP Service not running"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_f149f2b5-881f-4d4b-8e41-4b428e9e822d"
diagnosticScenario="DHCP Service not running"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# Guest VM Health Signal Insight
<!--issueDescription-->
## **DHCP Client service is not running and hence RDP connectivity is impacted**

The DHCP service is not running on the Virtual Machine. This could  happen due to:

1. DHCP service was set to disabled
    <br> The VM screenshot shows the OS fully loaded and waiting for the credentials

2. DHCP is crashing
    <br> If you pull the Guest OS Logs, you'll see that the VM is not starting the DHCP service

3. DHCP is hanging
    <br> On the Guest OS logs, you could find that the DHCP service is hanging or crashing or evidence that some other services are failing to start due to the DHCP service is disabled
<!--/issueDescription-->

## **Recommended Steps - Internal**
**Backup OS disk and set up the Troubleshooting environment**

Please refer to the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/TSG/Isolation_Bucket/DHCP_Client_service_is_not_starting) to RCA and view mitigation steps in detail.
