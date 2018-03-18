<properties
pageTitle="BFE Service"
description="BFE Service not running"
infoBubbleText="BFE Service not running"
service="microsoft.compute"
resource="virtualmachines"
authors="ramakk"
displayOrder=""
articleId="vmhealthsignal_10f4f09d-a1e8-4536-b167-8d2573fb4f0a"
diagnosticScenario="BFE services"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>


# Base Filtering Engine Service is not running
<!--issueDescription-->
Base Filtering Engine service is not running impacting network connectivity to the VM. This could  happen due to one of the below reasons:

1. The service was set to disabled

2. The service is crashing

3. The Service is hung

4. A dependent service is crashing/hung due to which this service is impacted as well.
<!--/issueDescription-->

## **Recommended Steps - Internal**

Please follow the guidance in the  [internal article](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Can%E2%80%99t_RDP-SSH/TSG/Isolation_Bucket/Base_Filtering_Engine_service_is_not_starting) to investigate and resolve the issue.
