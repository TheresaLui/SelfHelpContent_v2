<properties
	  pageTitle="Check if one or more DIPs are healthy"
	  description="Check if one or more DIPs are healthy"
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="fa3d56a9-2bc7-4bb2-b949-a6003c1d2963"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if one or more DIPs are healthy

Often customers cannot access their load balancer via the load balanced IP because all backend pool members (DIP) are down per the configured probe.

## Recommended Steps
1. In ASC, browse to the Diagnostics tab of the relevant load balancer and scroll down to &quot;DIP Availability&quot;. Click on the link for the relevant frontend IP and port. This will open a new tab with the DipAvailability_HealthProbeStatus Dashboard with the parameters filled out. If you are looking to root cause a prior issue, adjust the time parameter of the dashboard. Be sure to note time zones to ensure you are look at the right point in time.
2. On the top set of charts under &quot;Data Path Availability (VipAvailability)&quot;, look to see if there are any dips in VipAvailability and if so, see if there are jumps in FailureCount. If you see an increase in NoFowardingDip, the customer is unable to connect to their load balancer because all members of the backend pool were unhealthy.

