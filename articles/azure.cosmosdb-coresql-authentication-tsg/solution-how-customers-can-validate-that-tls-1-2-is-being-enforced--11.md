<properties
	  pageTitle="How customers can validate that TLS 1.2 is being enforced?"
	  description="How customers can validate that TLS 1.2 is being enforced?"
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
	  articleId="8cbece40-8f61-4827-9e09-72b3c429e55f"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# How customers can validate that TLS 1.2 is being enforced?

<!--issueDescription-->

Dear customer,

Some security scanners can point that TLS 1.0 is still available even after configuration is in place. Check below explanation from product group and tool to validate TLS 1.2 enforcement:

Cosmos is a multi-tenant service so we enable (at the service level) TLS 1.0 and up. But for the specified accounts if a request is made to them that is not TLS 1.2 it will be denied and never reach their service. The tool below performs that request for the customers (given a bit of data). Other TLS validation tooling does not take into account the multitenancy of a service and thus will report that Cosmos DB has TLS 1.0 and up enabled for their account, when in fact at the account level we do not.
https://github.com/Azure/cosmos-tls-scanner 

Thank you.

<!--/issueDescription-->

