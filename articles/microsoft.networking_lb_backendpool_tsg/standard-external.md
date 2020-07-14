<properties
	pageTitle="Check the VIP/DIP of Standard External LB"
	description="Check the VIP/DIP of Standard External LB"
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
	articleId="4af8436b-767f-444a-8499-330740d8d7da"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the VIP/DIP of Standard External LB

## **Recommended Steps**

We now know the SKU/facing direction of the Load Balancer we are troubleshooting. These steps will help you find the VIP/DIP for the load balancer

* Gather these details and input them below. We will need them later
* VIP
  * ASC: On the Load Balancers Properties page under 'Frontend IP Configurations' under 'Public IP Address'
  * Jarvis: run Get NRP Subscription Details
  * CTRL+f and search for the LBs name
  * Under 'properties' --> 'frontendipconfigurations' --> 'properties' --> 'publicIPAddress' you will see the Resource URI for the public IP associated to the LB
  * eg:/subscriptions/3ed4f01f-6e27-4724-93bf-e1001f78a63f/resourceGroups/RG01/providers/Microsoft.Network/publicIPAddresses/PublicBasicLB-ip
  * CTRL+f for the name of the public IP resource: eg: PublicBasicLB-ip
  * Under 'properties' --> 'ipAddress' you will see the VIP
* DIP:
  * DIPS can be found in ASC from the backend pool page of the load balancer resource
