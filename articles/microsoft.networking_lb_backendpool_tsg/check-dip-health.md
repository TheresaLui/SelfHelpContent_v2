<properties
	pageTitle="Check DIP Health"
	description="Check DIP Health"
	service="microsoft.network"
	resource="loadBalancers"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32588977"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="d61f3158-322f-4a06-b323-c256a638607a"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check for DIP availability issues

## **How DIP availability works**

* DIP Health refers to the Backend pool VM's response to the LB probes. When the customer reports that the load balancer isn't passing traffic to the backend VM, one of the first things we want to look at is whether the VM is reporting that it is healthy or not.
* The LB won't pass traffic to a backend VM if it is reporting unhealthy. We have several options to view this data including Jarvis Actions, Jarvis Dashboards, and mod-anp PowerShell commands.
* The method you use varies based on the sku/facing direction of the Load Balancer as well as which data you want. Generally, for things in the past (customer's VM stopped receiving traffic from the Load Balancer for a 5 minute period last night) use a Jarvis Dashboard.
* Use Jarvis Actions and PowerShell to see the health the Backend VM is currently reporting to the Load Balancer.

## **Check DIP Availability Dashboard**

## **Recommended Steps**

*Note: This Dashboard will work for ALL LB SKUs and facing directions. You only need the LB's VIP and Region.*

* Using Azure Support Center
	* Navigate to the Load Balancer in Resource Explorer --> Diagnostics Tab --> SLB DIP Status Dashboard.
* Using Jarvis if ASC isn't working follow the steps below.
  * In the upper left under 'Account' enter 'slbhp' followed by the region the LB is in. Example: 'slbhpeastus'
  * In the upper left under 'VipAddress' enter the VIP of the Load Balancer which you found in Step 2. Note: Sometimes as you type the VIP you will notice that a list populates in the dropdown. Sometimes your VIP will be in the list and sometimes it won't. After entering your VIP, hit Enter and the data should populate.
  * Update the time in the upper right by clicking the clock icon. Then enter the specific dates and times based on when the incident ocurred.

## **Recommended Documents**

* [Jarvis Link For DIP Health](https://jarvis-west.dc.ad.msft.net/dashboard/share/62D0DDB4?overrides=%5B{%22query%22:%22//dataSources%22,%22key%22:%22account%22,%22replacement%22:%22slbhpeastus%22},{%22query%22:%22//*%5Bid='VipPort'%5D%22,%22key%22:%22value%22,%22replacement%22:%22%22},{%22query%22:%22//*%5Bid='DipPort'%5D%22,%22key%22:%22value%22,%22replacement%22:%22%22},{%22query%22:%22//*%5Bid='VipAddress'%5D%22,%22key%22:%22value%22,%22replacement%22:%22100.120.50.37%22}%5D%20)
