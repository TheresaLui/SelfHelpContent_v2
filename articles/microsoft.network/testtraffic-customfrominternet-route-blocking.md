<properties
pageTitle="Traffic is altered by UDR"
description="Traffic is altered by UDR"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="TobyTu"
ms.author="Mario.Liu"
displayOrder=""
articleId="TestTrafficCustomFromInternetRouteBlocking"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# Traffic is altered by UDR

### <!--$VmName-->VmName<!--/$VmName-->: <!--$InsightTitle-->InsightTitle<!--/$InsightTitle-->

<!--issueDescription-->
We have identified a problem that prevents network traffic flowing from <!--$SourceIp-->SourceIp<!--/$SourceIp--> to virtual machine <!--$VmName-->VmName<!--/$VmName--> on port <!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->. Our diagnostics detected that the following condition exists:<br>

User-defined route tables have a route that is causing the issue.
<!--/issueDescription-->

## **Recommended Steps**

You can use [Next hop](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview) to learn which custom route alters the traffic flow.

If the routing method does not produce the desired result, examine the [User-defined route tables]( https://ms.portal.azure.com/#blade/HubsExtension/BrowseResource/resourceType/Microsoft.Network%2FrouteTables) to make sure that the routing is set up correctly. You can try to disassociate questionable [User-defined route tables]( https://ms.portal.azure.com/#blade/HubsExtension/BrowseResource/resourceType/Microsoft.Network%2FrouteTables) from the affected subnet to determine whether that resolves the issue.

### Tests executed

<!--$TestTrafficExecutionDetails-->TestTrafficExecutionDetails<!--/$TestTrafficExecutionDetails-->
