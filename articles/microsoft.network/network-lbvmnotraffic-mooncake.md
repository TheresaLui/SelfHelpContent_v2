<properties
    pageTitle="My Load Balanced VMs are not receiving traffic"
    description="My Load Balanced VMs are not receiving traffic"
    service="microsoft.network"
    resource="loadbalancers"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="16"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="2cad50d4-b6fc-4e78-af55-f6630bce7036"
	ownershipId="CloudNet_LoadBalancer"
/>

# My Load Balanced VMs are not receiving traffic

## **Recommended Steps**

If you have configured Load Balancer in your virtual network and have connectivity issues, try one or more of the following steps to resolve the issue.

1. Check if the Virtual Machines in the Load Balancer's Backend Pool are responding to Load Balancer Probe:

    1. Check if the Virtual Machines are up and available
    2. Check if the Virtual Machines are listening on the probe port
    3. Check if the Network Security Groups on load balancer backend pool VM allow traffic on probe port

2. Check if the Virtual Machines in the Load Balancer's Backend Pool are receiving and responding to traffic on data port:

    1. Check if the Virtual Machines are listening on the data port
    2. Check if the Network Security Groups on load balancer backend pool VM allow traffic on data port
    3. Check if a participating VM from backend pool is not trying to access the Internal Load Balancer VIP

## **Recommended Documents**

* [Troubleshoot Azure Load Balancer](https://docs.azure.cn/load-balancer/load-balancer-troubleshoot)
