<properties
	  pageTitle="Check if there was a healthy backend pool member at the time"
	  description="Check if there was a healthy backend pool member at the time"
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
	  articleId="89b7da74-2bd4-41a8-8987-4f5ed0d22cfc"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if there was a healthy backend pool member at the time

If the load balancer heath probe is detected down on all backend pool members, the load balancer will not have any backend pool member to forward the request to. As a result, the load balancer may appear to the customer to be unresponsive. This is especially true if the backend pool members respond to ping or management protocols (but not the application the load balancer probe is configured for). 

## Recommended Steps
1. In ASC, browse to the Diagnostics tab of the relevant load balancer and scroll down to ?DIP Availability?. Click on the link for the relevant frontend IP and port. This will open a new tab with the DipAvailability_HealthProbeStatus Dashboard with the parameters filled out. Adjust the time parameter of the dashboard. Be sure to note time zones to ensure you are look at the right point in time. 
2. On the top set of charts under &quot;Data Path Availability (VipAvailability),&quot; look to see if there are any dips in VipAvailability and if so, see if there are jumps in FailureCount. If you see an increase in NoFowardingDip, the customer is unable to connect to their load balancer because all members of the backend pool were unhealthy.
3. Scroll down to Health Probe Status (Dip Availability): Aggregated by Frontend-IP-Address : Frontend-Port -> Backend-IP-Address : Backend-Port. The middle graph will show the failure count reason. If you see the failure reason as ProbeTimeout, ConnectionTerminated, HttpStatusCodeError, or HttpEndpointUnreachable, these are indications of customer backend application/VM configuration failures.

If you see ProbeTimeout or HttpEndpointUnreachable, it is likely there was likely an issue with the customer?s application at the time. This is even more likely if it is currently working and the customer reports making no changes.

