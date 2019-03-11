<properties
pageTitle="NvaDiagnostic"
description="NvaDiagnostic"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="NvaDiagnosticsInsight"
diagnosticScenario="NvaDiagnosticsInsight"
selfHelpType="Diagnostics"
supportTopicIds="32584252, 32584251, 32584250, 32584249, 32547215"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public"
/>
# We found an issue related to a Network Virtual Appliance used in this connectivity path 
<!--issueDescription-->  
We have assessed the routing from the source VM **'<!--$SourceVM-->[SourceVM]<!--/$SourceVM-->'** to the destination resource with IP **<!--$DestinationIP-->[DestinationIP]<!--/$DestinationIP-->** and found there is a Network Virtual Appliance (NVA) named **'<!--$NvaVmName-->[NvaVmName]<!--/$NvaVmName-->'** managing the traffic. We ran some diagnostics on the detected scenario and found the following: 

- Checked Source Virtual Health: **<!--$SourceVmHealthStatus-->[SourceVmHealthStatus]<!--/$SourceVmHealthStatus-->** 
- Checked Network Virtual Appliance Health: **<!--$NvaHealthStatus-->[NvaHealthStatus]<!--/$NvaHealthStatus-->**
- Checked Destination VM Health (if applicable): **<!--$DestVmHealthStatus-->[DestVmHealthStatus]<!--/$DestVmHealthStatus-->**
- Checked IP Forwarding on the NVA: **<!--$IpFwdStatus-->[IpFwdStatus]<!--/$IpFwdStatus-->**
- Checked for Network Security Groups (NSGs) blocking traffic from source to NVA: **<!--$SourceToNvaNsgStatus-->[SourceToNvaNsgStatus]<!--/$SourceToNvaNsgStatus-->** 
- Checked for Network Security Groups (NSGs) blocking traffic from destination IP (**<!--$DestinationIP-->[DestinationIP]<!--/$DestinationIP-->**) to source: **<!--$DestinationToSourceNsgStatus-->[DestinationToSourceNsgStatus]<!--/$DestinationToSourceNsgStatus-->** <br><br>
See below for detailed steps on resolving detected issues.
<!--/issueDescription-->
## Steps to resolve detected issues:
<!--$ResolutionSteps-->[ResolutionSteps]<!--/$ResolutionSteps-->

