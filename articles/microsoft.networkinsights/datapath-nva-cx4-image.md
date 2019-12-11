<properties
pageTitle="Network Virtual Appliance (NVA) VM image with outdated drivers "
description="The VM is a Network Virtual Appliance (NVA) image with outdated network drivers."
infoBubbleText="VM image needs to be updated. See details on the right"
service="microsoft.compute"
resource="virtualmachines"
authors="rkrir"
ms.author="krisragh"
displayOrder="19"
articleId="AccelNetNvaCx4Insight"
diagnosticScenario="AccelNetNvaCx4Insight"
selfHelpType="resource"
supportTopicIds=""
cloudEnvironments="Public"
/>

If you have verified that the customer's impact is primarily due to a Network Virtual Appliance (NVA) image with outdated drivers, please adapt the root cause statement below. Please also double-check that the customer's VM version is in the list of unsupported images.

**NVA image publisher**|**Unsupported image versions**|**Supported image versions (customer should upgrade to these)**
:-----:|:-----:|:-----:
Cisco (Cisco-csr-1000v)|16.10.220190622, 16.10.120190108, 16.9.220181121|16.12.120190816 and higher
Barracudanetworks (Barracuda-ng-firewall)|8.0.0047501, 8.0.0047503|8.0.0047504 and higher
Arista-networks (vEos-router)|4.21.0, 4.21.3, 4.22.0|4.22.10 and higher
Paloaltonetworks (VM-Series)|9.0.1|9.0.4 and higher


# We ran diagnostics on your VM instance and found an issue. 

The VM with ID {VmId}, of version {VmVersion}, does not have the network drivers necessary to support Accelerated Networking on Azure's latest ConnectX-4 hardware. This may impact performance. Our partners have updated their Network Virtual Appliance (NVA) images to work with the latest hardware, and have published the updated images to Azure Marketplace. 

We are continuously working on improving the platform and apologize for any inconvenience this may have caused to you.

## **Recommended steps**

To avoid any impact to your current deployments, please upgrade your VM to the latest version in Azure Marketplace. Older VM versions are not affected.
