<properties
	pageTitle="Check the VIP/DIP for Basic Internal LB"
	description="Check the VIP/DIP for Basic Internal LB"
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
	articleId="22204287-73e0-456a-a01d-5d7a483d97c9"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the VIP/DIP for Basic Internal LB

## **Recommended Steps**

We now know the SKU/facing direction of the Load Balancer we are troubleshooting. These steps will help you find the VIP/DIP for the load balancer

* Gather these details and input them below. We will need them later
* First use ASC to get the Deployment ID of a VM that is behind the ILB
  * Go to Jarvis Actions --> Regional Network Manager --> Deployment --> Get all service instances from serviceId. or use first link below
  * In the Region field, select the region the VM is in.
  * In the Service ID field, paste in the VMs Deployment ID
  * Click Run
  * After it has ran, select the 'Messages' tab. Copy the id from the 'service instance id:' (Its almost identical to the deployment ID but has additional numbers at the end)
* Go to Actions --> Regional Network Manager --> Deployment --> Get Allocated resources for a given service instance (its two actions down from the last action we ran) or use second link below
  * Paste in the service instance id we got from the last action.
  * In the Results tab, ILB VIP is at the bottom

## **Recommended Documents**

* [Jarvis action to get all service instances from service id](https://jarvis-west.dc.ad.msft.net/7C641CFB?genevatraceguid=a2a6d496-6361-47d3-bb14-3733b555ca82)
* [Jarvis action to get allocated resources for a given service instance](https://jarvis-west.dc.ad.msft.net/AADD8808?genevatraceguid=f50e1c7d-22e5-4b78-b3d8-8261eca22b8e)
