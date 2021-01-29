<properties
	  pageTitle="Check if outbound next hop type is internet"
	  description="Check if outbound next hop type is internet"
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="61131703-f799-4949-a7e5-c470c7a24dd0"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if outbound next hop type is internet

The next hop type for public load balancers must be internet. If the customer overrides this via a UDR or a default route being advertised via ExpressRoute or VPN, external load balancers will not work for the VM?s subnet as return traffic will be sent to the customer?s on-premises or a custom NVA. On-premises and NVAs (behind different load balancers) will not be able to source the return traffic from the load balancer public IP as it the IP space owned and advertised to the internet by the Microsoft, not the customer?s organization.

## How to check for outbound next hop type

1. Browse to a backend pool member VM in ASC
2. Click the Diagnostics tab and scroll down to Test Traffic
Specify the following parameters:
Traffic Direction: Out
Source IP: Source IP of the backend pool member IP configuration specified in the load balancer rule name
Destination IP: 1.1.1.1
Destination Port: 443
Transport Protocol: The load balanced protocol. This should be TCP or UDP only.

The port is not super import as we are checking the routing layer and not the NSG layer. Click Run. In the results, click on Stateless Test (Routing Layer). Ensure that the rule name is RouteTargetInternet_<Number> though it will usually be RouteTargetInternet_0.

