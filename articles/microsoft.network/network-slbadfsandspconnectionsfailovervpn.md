<properties
	pageTitle="ADFS & SharePoint connections fail behind Load Balancer over VPN"
	description="ADFS & SharePoint connections fail behind Load Balancer over VPN"
	service="microsoft.network"
	resource="loadbalancer"
	authors="radwiv"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# ADFS & SharePoint connections fail behind Load Balancer over VPN

## **Recommended steps**
1.	Adjust ADFS servers’ MTU to 1350 instead of relying on PMTUD as the ILB does not support ICMP. 
2.	Use DNS load balancing.
3.	Use Application Gateway instead of ILB.
4.	Use a 3rd party network appliance available in Azure marketplace.
5.	Use a VIP instead of the ILB to move this traffic out of the VPN, hence not hitting the MTU restriction.
