<properties
	pageTitle="Check DIP Health"
	description="Check DIP Health"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber,mariliu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d61f3158-322f-4a06-b323-c256a638607a"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check for DIP availability issues

## **Recommended Steps**

Use "DIP Availability Dashboard" in Azure Support Center. 

Steps: Navigate to the problematic Load Balancer in Resource Explorer --> "Diagnostics" Tab --> DIP Availability --> SLB DIP Availability Dashboard for <LB's VIP>.

Please refer to this Wiki artilce if you need more details about [SLB DIP and VIP Health and Availability](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/139169/SLB-DIP-and-VIP-Health-and-Availability). It includes excellent information.

## **More information about how DIP availability works**

* DIP Health refers to the Backend pool VM's response to the LB probes. When the customer reports that the load balancer isn't passing traffic to the backend VM, one of the first things we want to look at is whether the VM is reporting that it is healthy or not.
* The LB won't pass traffic to a backend VM if it is reporting unhealthy. We have several options to view this data. The primary method is ASC. Other methods include Jarvis Actions, Jarvis Dashboards, and mod-anp PowerShell commands.
* The method you use varies based on the sku/facing direction of the Load Balancer as well as which data you want. Generally, for things in the past (customer's VM stopped receiving traffic from the Load Balancer for a 5 minute period last night) use a Jarvis Dashboard.
* Use ASC to see the health the Backend VM is currently reporting to the Load Balancer. If ASC doesn't work, use Jarvis Actions or PowerShell instead.
