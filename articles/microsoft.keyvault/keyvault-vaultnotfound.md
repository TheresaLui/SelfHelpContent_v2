<properties
	pageTitle="Key Vault recommendations"
	description="Key Vault recommendations are available"
	infoBubbleText="Vault name already taken."
	service="microsoft.keyvault"
	resource="vault"
	authors="osmuller"
	ms.author="osmuller"
	displayOrder=""
	articleId="keyvault-vaultnotfound"
	diagnosticScenario="keyvault-recommendations"
	selfHelpType="Diagnostics"
	supportTopicIds="32375295,32596891,32452742,32738117,32738118,32738116"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	ownershipId="AzureKeyVault_KeyVault"
/>

# You have Key Vault recommendations

<!--issueDescription-->
Your attempt to create a new key vault has failed since the name of the key vault is already in use. If you recently deleted a key vault with this name, it may still exist in the soft deleted state.
<!--/issueDescription-->

## **Recommended Steps**

1. If the vault was recently deleted please ask the vault owner to verify that the vault is not in a soft deleted state.

## **Recommended Documents**

Refer to the following documents to help with soft delete. 

* [Azure key vault soft delete](https://docs.microsoft.com/azure/key-vault/general/overview-soft-delete)
