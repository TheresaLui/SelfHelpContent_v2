<properties
pageTitle="Microsoft Azure has information regarding your Load Balancer"
description="Microsoft Azure has information regarding your Load Balancer"
infoBubbleText="Microsoft Azure has information regarding your Load Balancer. Please see details to the right."
service="microsoft.network"
resource="loadbalancer"
authors="chadmath, ramandhillon84"
ms.author="chadmat, rdhillon"
displayOrder=""
articleId="VmNotRespondingToLoadBalancerProbe"
diagnosticScenario="VmNotRespondingToLoadBalancerProbe"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
ownershipId="CloudNet_LoadBalancer"
/>

# Your Load Balancer probes are blocked by a Network Security Group
<!--issueDescription-->
We have found that the NSG '<!--$NetworkSecurityGroupName-->[NetworkSecurityGroupName]<!--/$NetworkSecurityGroupName-->' applied on your backend address pool '<!--$AddressPoolName-->[AddressPoolName]<!--/$AddressPoolName-->' for your loadbalancer '<!--$LoadBalancerName-->[LoadBalancerName]<!--/$LoadBalancerName-->' has a rule '<!--$RuleName-->[RuleName]<!--/$RuleName-->' that is blocking the load balancer probe IP 168.63.129.16 to your backend address pool resources. This has caused your load balancer to mark the backend pool resources as unhealthy and remove them from rotation. IP address 168.63.129.16 is a virtual public IP address, which in this case enables monitoring probes from the Azure load balancer to determine health state for VMs in a load balanced set.
<!--/issueDescription-->

## **Recommended Steps**

1. Open the [Azure portal](https://portal.azure.com) and browse to [Network Security Group blade](https://portal.azure.com/?feature.customportal=false#blade/HubsExtension/Resources/resourceType/Microsoft.Network%2FNetworkSecurityGroups)
2. Open your Network Security Group **'<!--$NetworkSecurityGroupName-->[NetworkSecurityGroupName]<!--/$NetworkSecurityGroupName-->'**
3. Add an **Allow** rule for IP address **168.63.129.16** that has a lower number (higher priority) than the Block rule
4. Save changes and check the Health Probe Status by going to Load Balancer Monitoring blade to view the backend pool health

## **Recommended Documents**
* Learn more about [Load Balancer health probes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview) and the [probe source IP address](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview#probesource)
* Learn more about [Load Balancer Monitoring](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics)

