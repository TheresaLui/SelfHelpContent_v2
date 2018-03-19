<properties
pageTitle="DHCP not running"
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

# DHCP Client service is not running
<!--issueDescription-->

The DHCP service is not running on the Virtual Machine. This could  happen due to one of the below reasons:

1. The service was set to disabled

2. The service is crashing

3. The Service is hung

4. A dependent service is crashing/hung due to which this service is impacted as well.

<!--/issueDescription-->

## **Recommended Steps - Internal**
**Backup OS disk and set up the Troubleshooting environment**

Please refer to the [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/TSG/Isolation_Bucket/DHCP_Client_service_is_not_starting) to RCA and view mitigation steps in detail.
