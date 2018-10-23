<properties
	pageTitle="My Load Balanced VMs are not receiving traffic"
	description="My Load Balanced VMs are not receiving traffic"
	service="microsoft.network"
	resource="loadbalancers"
	authors="radwiv"
	displayOrder="16"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# My Load Balanced VMs are not receiving traffic

## **Recommended steps**

If you have configured Load Balancer in your virtual network and have connectivity issues, try one or more of the below steps to resolve the issue.<br>

1. Check if the Virtual Machines in the Load Balancer's Backend Pool are responding to Load Balancer Probe<br>

    1. Check if the Virtual Machines are up and available.<br>
    2. Check if the Virtual Machines are listening on the probe port.<br>
    3. Check if the Network Security Groups on load balancer backend pool VM allow traffic on probe port.<br>

2. Check if the Virtual Machines in the Load Balancer's Backend Pool are receiving and responding to traffic on data port<br>

    1. Check if the Virtual Machines are listening on the data port.<br>
    2. Check if the Network Security Groups on load balancer backend pool VM allow traffic on data port.<br>
    3. Check if a participating VM from backend pool is not trying to access the Internal Load Balancer VIP.<br>

## **Recommended documents**

* [Troubleshoot Azure Load Balancer](https://docs.azure.cn/load-balancer/load-balancer-troubleshoot)
