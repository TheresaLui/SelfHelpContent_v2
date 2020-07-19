<properties
	pageTitle="Key Vault recommendations"
	description="Key Vault recommendations are available"
	infoBubbleText="Found an issue with Vault access policies"
	service="microsoft.keyvault"
	resource="vault"
	authors="osmuller"
	ms.author="osmuller"
	displayOrder=""
	articleId="keyvault-unauthorizedacl"
	diagnosticScenario="keyvault-recommendations"
	selfHelpType="Diagnostics"
	supportTopicIds="32375283"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	ownershipId="AzureKeyVault_KeyVault"
/>

# You have Key Vault recommendations

<!--issueDescription-->
The key vault has denied access to a user or application because the user or application did not have sufficient key vault access policy permissions to perform an operation on the key vault.
<!--/issueDescription-->

## **Recommended Steps**

1. Please ask the owner of this key vault to grant the correct permissions in the key vault access policies to this user or application 
2. If you are unsure what permissions must be granted to enable access or what operations were affected, please enable diagnostic logs on this key vault and look at the log entries or use Azure Monitor to examine any failed requests

## **Recommended Documents**

Refer to the following documents to help set up logging and use Azure Monitor. 

* [Azure monitor key vault](https://docs.microsoft.com/azure/azure-monitor/insights/azure-key-vault)
* [Azure key vault logging](https://docs.microsoft.com/azure/key-vault/key-vault-logging)
