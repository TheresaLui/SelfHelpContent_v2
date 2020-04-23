<properties
	pageTitle="Add UDR for the BE pool subnet"
	description="Add UDR for the BE pool subnet"
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
	articleId="e2792f08-10b8-47eb-9b66-4a8f29ace9ed"
	ownershipId="CloudNet_LoadBalancer"
/>

# Add UDR for the BE pool subnet

## **Recommended Steps**

* To repair this issue, create a UDR on the BE pool subnet with a route for 0.0.0.0/Internet