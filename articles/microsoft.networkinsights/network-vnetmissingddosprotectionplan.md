<properties
pageTitle="Microsoft Azure has information regarding your DDOS Protection Plan"
description="Microsoft Azure has information regarding your DDOS Protection Plan"
infoBubbleText="Microsoft Azure has information regarding your DDOS Protection Plan. Please see details to the right."
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="karenha"
displayOrder=""
articleId="VNetMissingDDoSProtectionPlan"
diagnosticScenario="VNetMissingDDoSProtectionPlan"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
ownershipId="CloudNet_AzureDDOSProtection"
/>
# Your virtual network is not associated with a DDoS Protection Standard Plan
<!--issueDescription-->
We have found that your Virtual Network, <!--$VirtualNetworkName-->[VirtualNetworkName]<!--/$VirtualNetworkName-->, is not associated with a DDoS Protection Standard Plan. To provide advanced DDoS protection, a DDoS Protection Standard Plan needs to be associated with this virtual network. A DDoS Protection Standard Plan protects resources in a virtual network including public IP addresses associated with virtual machines, load balancers and application gateways. When coupled with the Application Gateway web application firewall, DDoS Protection Standard can provide full layer 3 to layer 7 protection capability.
<!--/issueDescription-->

## **Recommended Steps**

To enable DDoS Protection on Virtual Networks, use the resources below:

* [How to enable DDoS for an existing Virtual Network](https://docs.microsoft.com/azure/virtual-network/manage-ddos-protection#enable-ddos-for-an-existing-virtual-network)
* [How to enable DDoS for a new virtual network](https://docs.microsoft.com/azure/virtual-network/manage-ddos-protection#enable-ddos-for-a-new-virtual-network)
* More information on [Application Gateway web application firewall](https://docs.microsoft.com/azure/application-gateway/application-gateway-web-application-firewall-overview)


