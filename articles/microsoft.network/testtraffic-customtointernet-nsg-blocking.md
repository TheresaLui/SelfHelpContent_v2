<properties
pageTitle="Traffic is blocked by NSG"
description="Traffic is blocked by NSG"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="spacest"
ms.author="Mario.Liu"
displayOrder=""
articleId="TestTrafficCustomToInternetNsgBlocking"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# Traffic is blocked by NSG

<!--issueDescription-->
We have identified a problem that prevents network traffic flowing from the <!--$VmName-->VmName<!--/$VmName--> virtual machine to <!--$DestinationIp-->DestinationIp<!--/$DestinationIp--> on port <!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->. Our diagnostics detected that the following condition exists:<br>

Network Security Group <!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName--> has a rule <!--$SecurityRuleName-->SecurityRuleName<!--/$SecurityRuleName--> that is causing the issue.  
<!--/issueDescription-->

## **Recommended Steps**

If the access control result is not the desired result, remove the <!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName--> network security group to allow network traffic to flow from the <!--$VmName-->VmName<!--/$VmName--> virtual machine to <!--$DestinationIp-->DestinationIp<!--/$DestinationIp--> on port <!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->. Or, you can create an OUTBOUND basic rule that has a higher priority (lower number) than have the existing rules that specify port <!--$DestinationPort-->DestinationPort<!--/$DestinationPort-->. To do this, follow these steps:

1. Open the [Azure portal](https://portal.azure.com) and browse to the [Network Security Group blade](https://portal.azure.com/?feature.customportal=false#blade/HubsExtension/Resources/resourceType/Microsoft.Network%2FNetworkSecurityGroups)
2. Open your **<!--$DestinationNsgName-->DestinationNsgName<!--/$DestinationNsgName-->** network security group
3. Add an **Allow** rule for **<!--$DestinationIp-->DestinationIp<!--/$DestinationIp-->** IP address that has a lower number (higher priority) than has the Block rule
4. Save the changes, and check the traffic status again

### Tests Executed

<!--$TestTrafficExecutionDetails-->TestTrafficExecutionDetails<!--/$TestTrafficExecutionDetails-->