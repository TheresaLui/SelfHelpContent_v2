<properties
	pageTitle="Check the VIP/DIP for Standard Internal LB"
	description="Check the VIP/DIP for Standard Internal LB"
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
	articleId="ef314bc4-c39c-4ab2-a35b-d9e15d7f8905"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the VIP/DIP for Standard Internal LB

## **Recommended Steps**

We now know the SKU/facing direction of the Load Balancer we are troubleshooting. These steps will help you find the VIP/DIP for the load balancer

* Gather these details and input them below. We will need them later
* You have to use Jarvis to find the VIP
* You cannot use the mod-anp commands (get-anpslbvipstate/get-anpilbvipstate) as these only work for the Basic SKU Load Balancer.
* To find the VIP on standard ILB, run get NRP Subscription.
* Jarvis Actions --> NRP --> NRP Subscription Operations --> Get NRP Subscription Details.
* Locate the ILB in the JSON output (CTRTL+f the LB name)
* Look through the output for the 'ipReservation' as seen in below code box

~~~json
ipReservation': {
reservedIPAddress: **20.185.106.242**,,
'reservationId': '8a8b5951-ede7-4e82-a19c-a13cdc7699e0',
}
~~~

## **Recommended Documents**

* [Jarvis action to find the VIP for standard internal load balancer](https://jarvis-west.dc.ad.msft.net/43808A00?genevatraceguid=306a7e53-d1d5-4d2b-9dbb-95277d33fb31)
