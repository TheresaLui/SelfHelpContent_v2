<properties
	pageTitle="Store credentials in Azure Key Vault"
	description="Store credentials for data store and computes in AKV"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="e77e0014-d0cb-4d49-a8e5-b5fc904811c2"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629445"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Store Credential in Azure Key Vault

__Note__: This feature relies on data factory service identity. Please make sure your data factory has one associated. See [_ADF Service Identity_](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity) for how to generate and retrieve ADF service identity.

## **Recommended Steps**

To reference a stored credential stored in Azure Key Vault, you need to:

1. Retrieve data factory service identity
1. Grant the service identity access to your Azure Key Vault
1. Create a linked service pointing to your Azure Key Vault
1. Create data store linked service, inside which reference the corresponding secret stored in key vault

## **Recommended Documents**

Store credentials in and retrieve from Azure Key Vault [Document](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault), including following sections: <br>

* [Prerequisites](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#prerequisites) <br>
* [Steps](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#steps) <br>
* [Azure Key Vault linked service](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#azure-key-vault-linked-service) <br>
* [Reference secret stored in key vault](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#reference-secret-stored-in-key-vault) <br>
