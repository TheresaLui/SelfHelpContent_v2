<properties
	pageTitle="Check the Loadbalancer Type"
	description="Check the Loadbalancer Type"
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
	articleId="81dfd316-b2c3-4279-a625-cc1c9cad0f2c"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the Loadbalancer Type

## **Recommended Steps**

* Check in Azure Support Center > Resource Explorer > Load Balancer > properties page
  * SKU will either be 'Basic' or 'Standard'
  * Facing Direction will either be 'Internal' or 'External'

* Check manually If ASC is not working
	* Jarvis Actions --> NRP --> NRP Subscription Operations --> Get NRP Subscription Details (see private link below)
  * Standard will have a SKU of V2
  * Internal will have a privateIPAddress and External will have a PublicIPAddress

## **Recommended Documents**

* [Jarvis Action for finding direction and SKU](https://jarvis-west.dc.ad.msft.net/39C6323B?genevatraceguid=7d5d13db-9e8b-446d-8b4c-e2aeb308c3d3)
