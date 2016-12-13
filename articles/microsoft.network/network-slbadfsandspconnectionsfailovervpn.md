<properties
	pageTitle="ADFS & SharePoint connections fail behind Load Balancer over VPN"
	description="ADFS & SharePoint connections fail behind Load Balancer over VPN"
	service="microsoft.network"
	resource="loadbalancers"
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
1.	Adjust ADFS servers’ Maximum Transmission Unit (MTU) to 1350 instead of relying on Path MTU Discovery (PMTUD) as the Internal Load Balancer (ILB) doesn't support PMTUD.
2.	Use a 3rd party network appliance available in Azure marketplace.
3.	Use an External Load Balancer (ELB/SLB) instead of the ILB to move this traffic out of the VPN, hence not hitting the MTU restriction.
