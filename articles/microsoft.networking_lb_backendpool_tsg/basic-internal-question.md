<properties
	pageTitle="Check if the traffic is between virtual networks in different regions aka GLOBALLY PEERED"
	description="Check if the traffic is between virtual networks in different regions aka GLOBALLY PEERED"
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
	articleId="9ea8167d-3372-4fb8-a8a2-f477d77390cd"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check if the traffic is between virtual networks in different regions aka GLOBALLY PEERED

## **Recommended Steps**

Check if the LB traffic traverse through different vnets over vnet peering. If that is the case please read the steps below. Otherwise disregard this step and skip it by choosing "Traffic is not globally peered". 

* Check if the vnet peering is between vnets in the same or different regions
* This can be accomplished by looking at the vnets that are peered in ASC
* And looking at the region those resources exist in
