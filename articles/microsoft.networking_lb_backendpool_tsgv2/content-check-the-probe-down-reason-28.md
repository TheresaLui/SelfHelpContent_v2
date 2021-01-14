<properties
	  pageTitle="Check the probe down reason"
	  description="Check the probe down reason"
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
	  articleId="d68ec4f2-c348-4b5f-aa43-41c357d6305c"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check the probe down reason

If you see that VIP availability is down due to NoFowardingDip, scroll down to Health Probe Status (Dip Availability): Aggregated by Frontend-IP-Address : Frontend-Port -> Backend-IP-Address : Backend-Port. The middle graph will show the failure count reason. If you see the failure reason as ProbeTimeout, HttpEndpointUnreachable, or ConnectionTerminated choose timeout.

