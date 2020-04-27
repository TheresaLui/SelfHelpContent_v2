<properties
	pageTitle="Check backend VM connectivity directly"
	description="Check backend VM connectivity directly"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c397f4ae-2986-432c-800a-1aac421db1d4"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check backend VM connectivity directly

## **Recommended Steps**

* Bypass the load balancer to validate there is connectivity directly to backend resources
* Check customer verbatim in Service Desk to see how customer answered the question "can you connect to the BE pool endpoints by-passing the LB" Y/N/?
* Have the customer identify another VM in the same VNet as the LB and login. Install PSPING (Windows) or hping (Linux) and validate they can connect.
* Syntax:
  * Windows: psping www.bing.com:80
  * Linux: hping -p 80 www.bing.com
