<properties
	  pageTitle="Check for issues in the client environment"
	  description="Check for issues in the client environment"
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
	  articleId="b31a3c3c-1475-44f0-9b95-92b852d84f6d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check for issues in the client environment

<!--issueDescription-->

Dear customer,

Kindly check for issues in the client environment:
* Majority of our Client are getting the "Service Unavailable" Exception,  this is due to High CPU on the Client Environment. Please ensure the CPU usage are monitored in 5 second interval. Anything greater than 5 seconds interval does not reveal High CPU usage.
* Small Subset of issue were due to Client Side Network Issue

a. No connections successful at all? Check local port firewalls - Direct requires a lot of opened Ports/IP Addresses to be exposed

b. Some failing at first, then more and more failing? SNAT issues - https://docs.microsoft.com/en-us/azure/cosmos-db/troubleshoot-dot-net-sdk#snat 

c. Just intermittent connectivity issues

Run 'netstat' and look for number of requests in TIME_WAIT state. Can indicate we're closing connections too much, which will exhaust the connection pool. Solution is to increase connection pool size (and file descriptors to make sure we can actually open more sockets) (or to scale out to limit requests per client sdk if they can't control connection pool size (like app service)). Tools to Suggest is to User Perfmon if its On-premise environment Engage the Azure respective services if the application is running in Azure Platform

Thank you.

<!--/issueDescription-->

