<properties
pageTitle="Traffic is blocked by NSG and altered by UDR"
description="Traffic is blocked by NSG and altered by UDR"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="spacest"
ms.author="Mario.Liu"
displayOrder=""
articleId="TestTrafficCustomToInternetNsgAndRouteBlocking"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# Traffic is blocked by NSG and altered by UDR

<!--issueDescription-->
We have identified a problem that prevents network traffic from the virtual machine <!--$VmName-->VmName<!--/$VmName--> to <!--$DestinationIp-->DestinationIp<!--/$DestinationIp--> on port <!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->. Our diagnostics detected that both of the following conditions exist:<br>

. Network security group "<!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName-->" has rule "<!--$SecurityRuleName-->SecurityRuleName<!--/$SecurityRuleName-->" that is causing this issue.<br>
. User-defined route tables have a route that is causing this issue.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the issue that is caused by the network security group, remove the network security group "<!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName-->" to allow network traffic to flow from the <!--$VmName-->VmName<!--/$VmName--> virtual machine to <!--$DestinationIp-->DestinationIp<!--/$DestinationIp--> on port <!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->. Or, you can create an OUTBOUND basic rule that has a higher priority (lower number) than have the existing rules that specify port <!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->.

To do this, follow these steps:

1. Open the [Azure portal](https://portal.azure.com) and browse to the [Network Security Group blade](https://portal.azure.com/?feature.customportal=false#blade/HubsExtension/Resources/resourceType/Microsoft.Network%2FNetworkSecurityGroups).
2. Open your <!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName--> network security group.
3. Add an **Allow** rule for the <!--$DestinationIp-->DestinationIp<!--/$DestinationIp--> IP address that has a lower number (higher priority) than has the Block rule
4. Save the changes, and check the traffic status again.

To resolve the routing issue with User-defined route tables, you can use [Next hop](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview) to find out which custom route is altering the traffic flow, and examine the [User-defined route tables]( https://ms.portal.azure.com/#blade/HubsExtension/BrowseResource/resourceType/Microsoft.Network%2FrouteTables) to make sure that the routing is set up correctly. You can try to disassociate questionable User-defined route tables from the affected subnet to determine whether that resolves the issue.

### **Tests Executed**

<!--$TestTrafficExecutionDetails-->TestTrafficExecutionDetails<!--/$TestTrafficExecutionDetails-->