<properties
	pageTitle="Ensure listening port and open NSG to allow source IP"
	description="Ensure listening port and open NSG to allow source IP"
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
	articleId="ad2c4a3d-120a-492f-b9a9-6319954864b0"
	ownershipId="CloudNet_LoadBalancer"
/>

# Ensure listening port and open NSG to allow source IP

Please have the customer complete the following:

* Ensure there is an application listening on the port
* Open up the NSG to the source IP in question
* If the backend pool contains Network Virtual Appliances (NVAs) reference this [NVA TSG](https://aka.ms/anpnvawiki) for additional troubleshooting steps.
