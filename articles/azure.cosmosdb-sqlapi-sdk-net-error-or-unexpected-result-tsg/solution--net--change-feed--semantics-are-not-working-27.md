<properties
	  pageTitle=".Net: Change Feed: Semantics are not working"
	  description=".Net: Change Feed: Semantics are not working"
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
	  articleId="34178366-a6d4-4f22-97b0-275ddc024a6b"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# .Net: Change Feed: Semantics are not working

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Investigation (not customer message):**
At least one semantics isn't working  

Example of Customer Statement *"We do deal with document to create and update in a single transaction where as change feed api is sending to the subscriber the latest updated document, hence missing the event triggered for creating the document. Another point is also change feed is not sending any event to subscribers when the document is being deleted by TTL setting"*   

## Customer message:
Dear customer,

The current implementation of the change feed only returns the latest state of a particular document and it does not return the history of all the updates for that document. Once the current feed caught up with the latest document, some updates of it could be returned as part of future feed responses (it all depends on the time to process the current feed and how often the document gets updated). 

For example given a document A that has an integer property "myInt" which has been updated with "1", "2", "3" values, if the query for the feeds starts sometimes after the the second update the feed my return "2" or "3", depending on how fast we process the rest of the feeds up to getting to the document A. If future updates to the document occur i.e. "4", "5", depending on how fast those updates happen and how fast the feed processing execute the customer might get both updates or only the last update, "5".

Document deletes including soft deletes (via TTL settings) are currently not captured as part of the change feed.
In the near future (sometime this year) we are planning to role out a new change feed feature that will capture a more extensive history of a Cosmos document that will include multiple updates and the deletes; the history might be limited to a certain timeline.

Thank you.

<!--/issueDescription-->

