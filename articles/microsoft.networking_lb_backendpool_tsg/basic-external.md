<properties
	pageTitle="Check the VIP/DIP for Basic External LB"
	description="Check the VIP/DIP for Basic External LB"
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
	articleId="3bab1fde-c04a-4815-9231-50d92fd76bab_basic"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the VIP/DIP for Basic External LB

## **Recommended Steps**

We now know the SKU/facing direction of the Load Balancer we are troubleshooting. These steps will help you find the VIP/DIP for the load balancer
Gather these details and input them below. We will need them later

* VIP
  * ASC: On the Load Balancer's Properties page under 'Frontend IP Configurations' under 'Public IP Address'
  * Jarvis: run Get NRP Subscription Details
  * CTRL+f and search for the LBs name
  * Under 'properties' --> 'frontendipconfigurations' --> 'properties' --> 'publicIPAddress' you will see the Resource URI for the public IP associated to the LB
  * eg:/subscriptions/3ed4f01f-6e27-4724-93bf-e1001f78a63f/resourceGroups/RG01/providers/Microsoft.Network/publicIPAddresses/PublicBasicLB-ip
  * CTRL+f for the name of the public IP resource: eg: PublicBasicLB-ip
  * Under 'properties' --> 'ipAddress' you will see the VIP
* DIP:
  * Now that you have the VIP you can use the PowerShell ANP command get-anpslbvipstate.
  * This command requires a single parameter, the LB's VIP.
  * Output will show the DIPs for the VMs in the LBs backend pool
