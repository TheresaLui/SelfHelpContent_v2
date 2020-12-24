<properties
	  pageTitle="Cosmos DB resources are missing / not listed issue"
	  description="Cosmos DB resources are missing / not listed issue"
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
	  articleId="c042d8ef-6887-43d3-864a-1fe963691c53"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Cosmos DB resources are missing / not listed issue

<!--issueDescription-->

Dear customer, 

Azure Cosmos DB resource governance can be implemented with Azure Policy. Customers can create Azure Policy assignments based on built-in or custom policy definitions.

If you have created a custom policy definition, then a policy assignment and when reviewing policy compliance in the Azure portal, existing Cosmos DB resources are missing or not listed under any compliance state, then:

** Check Cosmos DB resources within the scope of the policy assignment**
Policy assignments can be scoped to management group, subscription, or resource group. Azure Policy will only evaluate resources that are in the scope at which the assignment was created.

**Check the custom policy definition?s policy rules, or if Cosmos DB resource provider type policy aliases was used**
To check, the list of valid Cosmos DB policy aliases can be retrieved using the following Powershell command: Get-AzPolicyAlias -NamespaceMatch ?documentdb? | select namespace, resourcetype -ExpandProperty aliases

# Recommended Documents:
https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias?view=azps-4.7.0

# Other Useful Links: 
[Azure Policy Documentation](https://docs.microsoft.com/azure/governance/policy/)
[Sample Built-in Policy Definitions](https://docs.microsoft.com/azure/governance/policy/samples/built-in-policies#cosmos-db)
[Sample Custom Policy Definitions](https://github.com/Azure/azure-policy/tree/master/samples/CosmosDB)

Thank you.


<!--/issueDescription-->

