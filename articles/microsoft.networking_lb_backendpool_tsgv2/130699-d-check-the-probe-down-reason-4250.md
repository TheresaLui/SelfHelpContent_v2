<properties
 pageTitle="Check the probe down reason"
 description="Check the probe down reason"
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
 articleId="63fd7f6b-b088-49b4-b5c5-5b9acefe4250"
 ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check the probe down reason

If you see that VIP availability is down due to NoFowardingDip, scroll down to Health Probe Status (Dip Availability): Aggregated by Frontend-IP-Address : Frontend-Port -> Backend-IP-Address : Backend-Port. The middle graph will show the failure count reason. If you see the failure reason as ProbeTimeout, HttpEndpointUnreachable, or ConnectionTerminated choose timeout.