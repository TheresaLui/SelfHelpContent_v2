<properties
	pageTitle="Key Vault recommendations"
	description="Key Vault recommendations are available"
	infoBubbleText="Found a possible issue with the vault's firewall settings"
	service="microsoft.keyvault"
	resource="vault"
	authors="osmuller"
	ms.author="osmuller"
	displayOrder=""
	articleId="keyvault-unauthorizedfirewall"
	diagnosticScenario="keyvault-recommendations"
	selfHelpType="Diagnostics"
    supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	ownershipId="AzureKeyVault_KeyVault"
/>

# You have Key Vault recommendations

<!--issueDescription-->
The key vault has denied access to a user or application in the time range you have entered, since the user or application was not allowed through the Key Vault firewall.
<!--/issueDescription-->

## **Recommended Steps**

1. Please ask the owner of this key vault to and add the correct IP Address or vNet configuration to the Key Vault firewall
2. If you are unsure what firewall configuration changes need to be made or what operations were affected, please enable diagnostic logs on this key vault and look at the log entries or use Azure Monitor to examine any failed requests

## **Recommended Documents**

Refer to the following documents to help set up logging and use Azure Monitor. 

* [Azure monitor key vault](https://docs.microsoft.com/azure/azure-monitor/insights/azure-key-vault)
* [Azure key vault logging](https://docs.microsoft.com/azure/key-vault/key-vault-logging)
