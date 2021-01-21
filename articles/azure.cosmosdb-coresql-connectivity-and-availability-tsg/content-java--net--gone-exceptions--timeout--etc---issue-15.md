<properties
	  pageTitle="Java/.Net (Gone exceptions, Timeout, etc.) issue"
	  description="Java/.Net (Gone exceptions, Timeout, etc.) issue"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="774ef46a-0acd-4947-8b18-b987a8995b90"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Java/.Net (Gone exceptions, Timeout, etc.) issue

For Java SDK: Confirm with customer that he has followed this steps: https://docs.microsoft.com/en-us/azure/cosmos-db/troubleshoot-java-async-sdk
If no, point it out to them that it can help them troubleshoot on their own in the future, but you can walk through the steps below.

**Is it failing across multiple backend clients at the same time?**   
 **If yes**. This is indicative of an issue not in the SDK, but between the SDK and the backend service. If you've checked for backend service issues, then it's worth looping in Azure Networking to look for a cause. Also ask whether they are using any Proxies/VNET firewall applicances/etc. that could cause issues.

 **If no**, check for issues in the client environment:
* Majority of our Client are getting the "Service Unavailable" Exception is due to High CPU on the Client Environment. Also, ensure the CPU usage are monitored in 5 second interval.  Anything greater than 5 seconds interval does not reveal High CPU usage.
* Small Subset of issue were due to Client Side Network Issue

a. No connections successful at all?
Check local port firewalls - Direct requires a lot of opened Ports/IP Addresses to be exposed

b. Some failing at first, then more and more failing?
SNAT issues - https://docs.microsoft.com/en-us/azure/cosmos-db/troubleshoot-dot-net-sdk#snat

c. Just intermittent connectivity issues
Run 'netstat' and look for number of requests in TIME_WAIT state. Can indicate we're closing connections too much, which will exhaust the connection pool. Solution is to increase connection pool size (and file descriptors to make sure we can actually open more sockets) (or to scale out to limit requests per client sdk if they can't control connection pool size (like app service)).
Tools to Suggest is to User Perfmon if its On-premise environment
Engage the Azure respective services if the application is running in Azure Platform


