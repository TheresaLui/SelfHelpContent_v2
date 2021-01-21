<properties
	  pageTitle="How to Allow List Cosmos DB IP in the On Premise environment issue"
	  description="How to Allow List Cosmos DB IP in the On Premise environment issue"
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
	  articleId="dd8f9cdf-fc4c-448b-8d48-61d63d51cfcd"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# How to "Allow List" Cosmos DB IP in the On Premise environment issue

<!--issueDescription-->

Dear customer,

There are situations where you need to "allow list" your  internal firewall to allow access to the Cosmos DB Endpoints.  This can be done for both Gateway Connection or Direct Connections.

The allow listing does require IP address to be known to enable on your environment.  But the issue becomes complicated when the IP address is not Static and also direct connection reaches to the nodes IPs which might change based on the partition migration or partition split.  Also, the Cosmos DB IP address are  dynamic. Having said that the IP address is not changed very often.

Azure does publishes the Public IP ranges for each **Services with region information weekly**.  The user can download these IP and automate the firewall rule using the IP address.

* [Azure Service Tags JSON - Public](https://www.microsoft.com/en-us/download/details.aspx?id=56519)
* [Azure Service Tags JSON - US cloud](https://www.microsoft.com/en-us/download/details.aspx?id=57063)
* [Azure Service Tags JSON - Germany cloud](https://www.microsoft.com/en-us/download/details.aspx?id=57064)
* [Azure Service Tags JSON - China cloud?](https://www.microsoft.com/en-us/download/details.aspx?id=57062) 
 
**Caveats**
The IP address is refreshed weekly. So the client is responsible to manage the refresh.
The connectivity from On premise or non-Azure Region would add latency to the application.

Thank you.

<!--/issueDescription-->

