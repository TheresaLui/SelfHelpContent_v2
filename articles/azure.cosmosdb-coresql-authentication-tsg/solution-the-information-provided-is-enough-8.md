<properties
	  pageTitle="The information provided is enough"
	  description="The information provided is enough"
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
	  articleId="facdd827-b64e-4155-9904-ce4086f72a35"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# The information provided is enough

<!--issueDescription-->

Dear customer,

Cosmos DB supports TLS 1.2 and enforcement is based on the below factors
- The account should be enabled to only allow TLS 1.2 connection
- The Client SDK Version  

The enforcement plan is as follows
- All **new accounts created on or after 29th July 2020** would be **enforcing the connection** to be TLS 1.2
- All legacy database account  to which a client is using TLS 1.2 would be migrated to enforce the TLS 1.2 seamlessly.  This means any connection using TLS version lower than 1.2 will be rejected after the migration and the client would get a clear error message.
- Any legacy database account to which the client are not using TLS 1.2 would continue to work fine and no enforcement would be applied

Thank you.

<!--/issueDescription-->

