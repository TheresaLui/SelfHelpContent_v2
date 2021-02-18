<properties
 pageTitle="Check if load balance rule has floating IP enabled"
 description="Check if load balance rule has floating IP enabled"
 service="Microsoft.Network"
 resource="Microsoft.Network/loadBalancers"
 authors="Centennial_CloudNet_LoadBalancer"
 ms.author="Centennial_CloudNet_LoadBalancer"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="ec71ffa4-324b-4333-be49-bb4f4c5c8446"
 ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if load balance rule has floating IP enabled

## About Floating IP
Customers can specify floating IP in their load balancer rule configuration. This cases the load balancer to not DNAT their front-end IP address to the Virtual Machine DIP. Frequently, customers enable this when using clustering solutions such as SQL AlwaysOn and Kubernetes (K8s). These technologies configure the guest OS to accept communications to the front-end IP address in addition to the VM DIP. If the customer does not configure their guest OS to accept connections to the front-end IP address, connections will fail. 

Sometimes customers incorrectly enable this option. If you notice that the customer has the option enabled check with the customer to ensure that what they configured is what they intended. Have them validate they have a clustering technology properly configured or a loopback adapter configured with the front-end IP. If the customer does not know what you are talking about, chances are they incorrectly configured floating IP and they should disable it.

## Recommended Steps

1. Find the Load Balancer in Resource Explorer in Azure Support Center
2. Find the load balancing rules used for the customer solution and expand
3. Check the property "Enable Floating IP"

For more information on Floating IPs check this Microsoft Docs Resource below

### Recommended Documents

* [backend port reuse by using Floating IP](https://docs.microsoft.com/azure/load-balancer/load-balancer-multivip-overview#rule-type-2-backend-port-reuse-by-using-floating-ip)
