<properties
 pageTitle="Check if load balancer probe IP is blocked by NSG"
 description="Check if load balancer probe IP is blocked by NSG"
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
 articleId="cce95a95-558e-4bb8-8f68-f46797dac7f7"
 ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if load balancer probe IP is blocked by NSG

# How load balancer health probes work
The SLB Host Plugin running on all Azure nodes sends the load balancer probes to all VMs that are running on it. Once the probe traffic gets to the guest OS, it appears to be sourced from the IP address 168.63.129.16. NSGs have a default rule to allow this communication (rule priority 65001, rule name AllowAzureLoadBalancerInBound). If the customer has a rule with a lower priority value (meaning it gets evaluated first), the probe traffic will be blocked by the NSG and the health probe will appear down. Check for this condition using the steps below. The probe configuration is up to the customer. It can be a TCP ping or an HTTP GET request. The VM will be probed down if the TCP ping times out or if the HTTP response code is a non-200 series.

To remedy this, the customer must add an inbound rule with higher priority (lower number) to allow traffic from source tag AzureLoadBalancer.

## Recommended Steps

* Using Resource Explorer in Azure Support Center, review the probe configuration for the load balancing rule in the load balancer properties.
* Navigate to a VM in the backend pool of the load balancing rule in question (this is in the load balancer resource)
* In the VM resource, go to the Diagnostics tab and scroll down to the TestTraffic tool
* Run TestTraffic with the following parameters:
Direction: InternetIn
Source IP: 168.63.129.16
Source Port: 2345
Destination IP: <VM IP>
Destination port: <Port customer configured for their probe or 80/443 for HTTP/HTTPS>
Protocol: TCP

In the result, browse to “Stateful Test (NSG Layer)” to see if the traffic is allowed or blocked.

### For more public documentation, reference these Microsoft Docs:
https://docs.microsoft.com/azure/virtual-network/what-is-ip-address-168-63-129-16
https://docs.microsoft.com/azure/virtual-network/service-tags-overview"
