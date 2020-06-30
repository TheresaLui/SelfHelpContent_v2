<properties
	pageTitle="Check the MUX for Basic External LB"
	description="Check the MUX for Basic External LB"
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
	articleId="b540ddf2-8f2c-4298-8e4f-be90c88a1e9d"
	ownershipId="CloudNet_LoadBalancer"
/>

# How to check the MUX for Basic External LB

## **Recommended Steps**

**Note: This works for both IPv4 and IPv6**

* Using the VIP as input, run the powershell command 'Get-anpslbvipstate -VIP $vip'. You will receive a bunch of output.
* Towards the bottom you'll see:

~~~powershell
SLB VIP State:,
OwnerSLB: SLB_BL5PrdApp01-N <----------- This is what we're looking for, the VIP Mux Tenant,
OwnerSLBVip: 40.117.87.254,
STATE ON SLBM:,
CurrentStatus: Achieved,
EndpointStateAchieved: True,
SnatStateAchieved: True
~~~
