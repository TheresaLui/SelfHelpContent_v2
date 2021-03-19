<properties
 pageTitle="Check if there was a healthy backend pool member at the time"
 description="Check if there was a healthy backend pool member at the time"
 service="Microsoft.Network"
 resource="Microsoft.Network/loadBalancers"
 authors="Centennial_CloudNet_LoadBalancer"
 ms.author="Centennial_CloudNet_LoadBalancer"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="e6c36597-edd6-4398-8672-bc5a7e57671a"
 ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if there was a healthy backend pool member at the time

If the load balancer heath probe is detected down on all backend pool members, the load balancer will not have any backend pool member to forward the request to. As a result, the load balancer may appear to the customer to be unresponsive. This is especially true if the backend pool members respond to ping or management protocols (but not the application the load balancer probe is configured for). 

## Recommended Steps
1. In ASC, browse to the Diagnostics tab of the relevant load balancer and scroll down to "DIP Availability". Click on the link for the relevant frontend IP and port. This will open a new tab with the DipAvailability_HealthProbeStatus Dashboard with the parameters filled out. Adjust the time parameter of the dashboard. Be sure to note time zones to ensure you are look at the right point in time. 
2. On the top set of charts under "Data Path Availability (VipAvailability)", look to see if there are any dips in VipAvailability and if so, see if there are jumps in FailureCount. If you see an increase in NoFowardingDip, the customer is unable to connect to their load balancer because all members of the backend pool were unhealthy.

