<properties
pageTitle="Microsoft Azure has information regarding your Load Balancer"
description="Microsoft Azure has information regarding your Load Balancer"
infoBubbleText="Microsoft Azure has information regarding your Load Balancer. Please see details to the right."
service="microsoft.network"
resource="loadbalancer"
authors="chadmath, rdhillon"
displayOrder=""
articleId="VmNotRespondingToLoadBalancerProbe"
diagnosticScenario="VmNotRespondingToLoadBalancerProbe"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Your Load Balancer probes are blocked by a Network Security Group
<!--issueDescription-->
We have found that the  NSG **'<!--$nsg-->[nsg]<!--/$nsg-->'** applied on your backend address pool **'<!--$backendpool-->[backendpool]<!--/$backendpool-->'** for your loadbalancer **'<!--$loadbalancer-->[loadbalancer]<!--/$loadbalancer-->'** is **blocking the load balancer probe IP 168.63.129.16** to your backend address pool resources. This has caused your load balancer to mark the backend pool resources as unhealthy and remove them from rotation.
<!--/issueDescription-->

## **Mitigation & More Information**
To resolve this issue:

1. Open the [Azure portal](https://portal.azure.com)
2. Browse to your Network Security Group **'<!--$nsg-->[nsg]<!--/$nsg-->'**
3. Add an Allow rule for IP addrses **168.63.129.16** that has a lower number (higher priority) than the Block rule.
4. Save changes and check the Health Probe Status by going to Load Balancer Monitoring blade to view the backend pool health.

Learn more about [Load Balancer health probes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview) and the [probe source IP address](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview#probesource).

Learn more about [Load Balancer Monitoring](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics).

