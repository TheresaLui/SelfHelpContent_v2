<properties
	pageTitle="Customer Traceroute"
	description="Customer Traceroute"
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
	articleId="ceb94c8f-85cf-4cc4-adc9-d2a7ec71e61c"
	ownershipId="CloudNet_LoadBalancer"
/>

# Customer Traceroute

## **Recommended Steps**

* If customer is able to bypass LB and access VM directly, then there are no issues with OS firewall and service listening on respective ports. Have the customer perform a traceroute and ensure there is a network path to the customer VIP
