<properties
	pageTitle="The response on endpoints is slow or varies a lot"
	description="The response on endpoints is slow or varies a lot"
	service="microsoft.network"
	resource="trafficmanagerprofiles"
	authors="radwiv"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="f5f90671-ebc6-4ede-b399-736c64382616"
	ownershipId="CloudNet_TrafficManager"
/>

# The response on endpoints is slow or varies a lot

Traffic Manager operates at the DNS layer to pick the best endpoint for a given request. The endpoints are picked based on the routing type you selected.
Once the endpoint is selected, the client connects to it directly and Traffic Manager doesn't get in the flow.

## **Recommended steps**

1. If the endpoint is an Azure resource, test the probe path in a browser and see if that makes any improvements.
2. If the performance continues to remain slow, run nslookup on the domain name that points to the traffic manager. This will provide the location of DNS server.
3. Refer to "Diagnose and Solve problems" section of that service in the Azure Portal.


## **Recommended documents**
[Windows Azure Traffic Manager Performance Impact](https://blogs.msdn.microsoft.com/kwill/2013/09/17/windows-azure-traffic-manager-performance-impact)
