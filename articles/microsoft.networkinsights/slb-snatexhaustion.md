<properties
pageTitle="Microsoft Azure has information regarding your Load Balancer"
description="Microsoft Azure has information regarding your Load Balancer"
infoBubbleText="Microsoft Azure has information regarding your Load Balancer. Please see details to the right."
service="microsoft.network"
resource="loadbalancer"
authors="rdhillon"
displayOrder=""
articleId="LoadBalancerConnectionsFailing"
diagnosticScenario="LoadBalancerConnectionsFailing"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# You are exhausting the SNAT ports available to your instances
<!--issueDescription-->
We have found that some instances in the backend pool **'<!--$AddressPoolName-->[AddressPoolName]<!--/$AddressPoolName-->'** of your load balancer **'<!--$LoadBalancerName-->[LoadBalancerName]<!--/$LoadBalancerName-->'** have exhausted the allocated SNAT ports for initiating outbound connections and might be experiencing outbound connection failures as a result.
<!--/issueDescription-->

## **Recommended options**
1. Modify your application to reuse connections.
2. Modify your application to use connection pooling.
3. Modify your application to use less aggressive retry logic.
4. Scale out by adding more instances in the backend pool of the load balancer if the instances are less than the pool size boundary as specified in the [Load Balancer Outbound connections](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#preallocatedports).
5. If it is a Standartd SKU Load Balancer, then try adding more frontend IP Addresses to increase the SNAT Port allocation.
6. Use [Outbound Rules](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-rules-overview) for a more customized SNAT port allocation to the instances.
7. Use [Instance Level Public IPs](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-instance-level-public-ip) for the instances that need to make exceptionally large number of outbound connections.

## **Recommended documents**
* Learn more about [Load Balancer Outbound connections](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections) and the [outbound Rules](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-rules-overview).
* Learn more about [Load Balancer Monitoring](https://docs.microsoft.com/azure/load-balancer/load-balancer-standard-diagnostics) to check the **SNAT connection** and **SNAT Port** metrics.
