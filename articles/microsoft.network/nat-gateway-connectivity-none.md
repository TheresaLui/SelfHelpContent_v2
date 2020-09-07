<properties
    pageTitle="No outbound connectivity"
    description="Troubleshoot no outbound connectivity of NAT gateway resource"
    service="microsoft.network"
    resource="natgateways"
    authors="christiankuhtz"
    ms.author="christiankuhtz"
    displayOrder="11"
    selfHelpType="resource"
    articleId="nat-gateway-connectivity-none-md"
    resourceTags=""
    productPesIds="16838"
    supportTopicIds="32681719"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="CloudNet_VirtualNetworkNAT"
/>

# NAT gateway - No outbound connectivity troubleshooting

## **Recommended Steps**

Check the following:

1. Does the NAT gateway resource have at least one public IP resource or one public IP prefix resource? You must at least have one IP address associated with the NAT gateway for it to be able to provide outbound connectivity.

2. Are you using TCP and UDP IP protocols? [NAT gateways do not provide ICMP connectivity](https://docs.microsoft.com/azure/virtual-network/troubleshoot-nat#icmp-ping-is-failing).

2. Check if you are experiencing SNAT exhaustion? Details can be found in this [troubleshooting](https://docs.microsoft.com/azure/virtual-network/troubleshoot-nat) document.

3. Are you using an internal Standard load balancer? Check whether the NAT gateway is actually configured on the subnet where the VM's in the internal load balancer's backend pool are.  Outbound connectivity does not exist behind an internal Standard load balancer.

4. Does the virtual network have a user-defined route (UDR) defined? Check the configuration of the subnet's UDRs. A misconfigured UDR can override the NAT gateway by preventing traffic from reaching the NAT gateway resource.

## **Recommended Documents**

* [Troubleshooting](https://docs.microsoft.com/azure/virtual-network/troubleshoot-nat)
