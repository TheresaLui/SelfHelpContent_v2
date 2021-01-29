<properties
	  pageTitle="Deny is not working issue"
	  description="Deny is not working issue"
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
	  articleId="5a27a8f0-b77f-4131-bd2e-c43b6137471d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Deny is not working issue

<!--issueDescription-->

Dear customer, 

Azure Cosmos DB resource governance can be implemented with Azure Policy. Customers can create Azure Policy assignments based on built-in or custom policy definitions.

If you have created a custom policy definition and assignment to deny creation of Cosmos DB resources (e.g. databases, keyspaces, graphs, tables, or child resources of any of those) based on checks like the requested throughput exceeding a maximum allowed value. But people are still able to create these resources. We would like to inform that this is a current issue in the Cosmos DB resource provider. Policy rules based on certain resource attributes will not work at this time, as the aliases in question do not yet exist on the resources being created, so policy evaluation sees those alias values as null, so create is not denied. The Cosmos DB Product Group is addressing this issue by updating the Resource Provider to emit correct aliases that will not evaluate as null during resource create. This will permit deny effects to work correctly. The expectation is that when Azure Policy support GAs (Build timeframe) this issue will have been mitigated, and policy effects like deny will work correctly at child resource create.

# Recommended Documents:
[Azure Policy Documentation](https://docs.microsoft.com/azure/governance/policy/)
[Sample Built-in Policy Definitions](https://docs.microsoft.com/azure/governance/policy/samples/built-in-policies#cosmos-db)
[Sample Custom Policy Definitions](https://github.com/Azure/azure-policy/tree/master/samples/CosmosDB)

Thank you for your comprehension.

<!--/issueDescription-->

