<properties
pageTitle="Microsoft Azure has information regarding your Load Balancer"
description="Microsoft Azure has information regarding your Load Balancer"
infoBubbleText="Microsoft Azure has information regarding your Load Balancer. Please see details to the right."
service="microsoft.network"
resource="loadbalancer"
authors="rdhillon"
displayOrder=""
articleId="LoadBalancerHasNoBackendAddressPoolsWIthIpConfigsDefined"
diagnosticScenario="LoadBalancerHasNoBackendAddressPoolsWIthIpConfigsDefined"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Your Load Balancer has no backend pools with IP Configs defined
<!--issueDescription-->
We have found that the your load balancer **'<!--$loadbalancer-->[loadbalancer]<!--/$loadbalancer-->'** has no backend pool resources with valid IP configuration, and the backend pools will be marked unavailable.
<!--/issueDescription-->

## **Mitigation & More Information**
To resolve this issue:

Add one or more Virtual Machines or Virtual Machine Scale Set Instances in the backend pool of your load balancer, and make sure the instances are configured to respond to the load balancer health probe as well as over the service port(s).

Learn more about [Load Balancer configuration](https://docs.microsoft.com/azure/load-balancer/tutorial-load-balancer-standard-manage-portal) and the [Load Balancer health probes](https://docs.microsoft.com/azure/load-balancer/load-balancer-custom-probe-overview).

Learn more about [Load Balancer Monitoring](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics).
