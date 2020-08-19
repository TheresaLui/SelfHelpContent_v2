<properties
	pageTitle="Check if there were VIP availability issues for Standard External LB"
	description="Check if there were VIP availability issues for Standard External LB"
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
	articleId="811ad9ff-73cd-494e-8838-5bb57a80bffd"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check if there were VIP availability issues for Standard External LB

## **Recommended Steps**

**Note: This works for both IPv4 and IPv6**

* Using the VIP for the LB
  * Open up this Jarvis Dashboard at the link below
  * Click the settings cog wheel next to 'Vip Availability'
  * Under Account, select the region the SLB is in. Naming is 'slbv2' followed by the Region. Ex. Slbv2eastus
  * Under dimensions, select 'non-indexed'
  * Below that, select 'VipAddress'
  * Enter the SLB VIP in the filter box
  * Select the appropriate time frame
  * Apply the settings
* A graph will be displayed showing VIP availability
* If you see any drops, mouse over the big drop and the report will tell you the availability percentage.
* VIPs are hosted by a pool and any number below 100% means some percentage of MUXs stopped advertising the VIP.
* However, there were still other MUXs in the pool servicing this VIP so the customer shouldn't experience any issues due to this.
  
**NOTE**: We need to be careful in consuming this dashboard. The screenshot above was taken from a healthy LB with no issues. Any findings from this dashboard will need to have additional data to support any claim that VIP availability is the cause of an issue. VIP availability is rarely the cause of Load Balancer issues but having this dashboard available could help if you are stuck while troubleshooting.

## **Recommended Documents**

* [Jarvis dashboard for VIP availability](https://jarvis-west.dc.ad.msft.net/dashboard/share/BB1037B1)
