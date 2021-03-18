<properties
pageTitle="Traffic is blocked by NSG and altered by UDR"
description="Traffic is blocked by NSG and altered by UDR"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="TobyTu"
ms.author="Mario.Liu"
displayOrder=""
articleId="TestTrafficCustomFromInternetNsgAndRouteBlocking"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# Traffic is blocked by Network Security Group and altered by User-defined route tables

<!--issueDescription-->
We have identified a problem that prevents network traffic flowing from a sample public IP address <!--$SourceIp-->SourceIp<!--/$SourceIp--> to the **<!--$VmName-->VmName<!--/$VmName-->** virtual machine on port **<!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->**. Our diagnostics detected that both of the following conditions exist:<br>

* Network security group **"<!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName-->"** has rule **"<!--$SecurityRuleName-->SecurityRuleName<!--/$SecurityRuleName-->"** that is causing this issue.<br>
* User-defined route tables have a route that is causing this issue.
<!--/issueDescription-->

## **Recommended Steps**

* To resolve the issue caused by the network security group, remove the **<!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName-->** network security group to allow network traffic to flow from public IP address(es) to the virtual machine **<!--$VmName-->VmName<!--/$VmName-->** on port **<!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->**. Or, create an INBOUND basic rule that has a higher priority (lower number) than the existing rules that specify port **<!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->**.

   To do this, follow these steps:

   1. Open the [Azure portal](https://portal.azure.com) and go to the [Network Security Group blade](https://portal.azure.com/?feature.customportal=false#blade/HubsExtension/Resources/resourceType/Microsoft.Network%2FNetworkSecurityGroups).
   2. Open your **<!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName-->** network security group.
   3. Add an **Allow** rule for public IP addresses (for example, <!--$SourceIp-->SourceIp<!--/$SourceIp-->) which has a lower number (higher priority) than the Deny rule **<!--$SecurityRuleName-->SecurityRuleName<!--/$SecurityRuleName-->**.
   4. Save the changes, and check the traffic status again.

* To resolve the routing issue with user-defined route tables, [view effective routes](https://docs.microsoft.com/azure/virtual-network/manage-route-table#view-effective-routes) on the network interface that is attached to virtual machine <!--$VmName-->VmName<!--/$VmName-->. You can also use [Next hop](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview) to learn which custom route alters the traffic flow. If the routing method does not produce the desired result, examine the [User-defined route tables]( https://ms.portal.azure.com/#blade/HubsExtension/BrowseResource/resourceType/Microsoft.Network%2FrouteTables) to make sure that the routing is set up correctly. You can try to [dissociate](https://docs.microsoft.com/azure/virtual-network/manage-route-table#dissociate-a-route-table-from-a-subnet) questionable [User-defined route tables](https://ms.portal.azure.com/#blade/HubsExtension/BrowseResource/resourceType/Microsoft.Network%2FrouteTables) from the affected subnet to determine whether that resolves the issue.

### **Tests Executed**

<!--$TestTrafficExecutionDetails-->TestTrafficExecutionDetails<!--/$TestTrafficExecutionDetails-->
