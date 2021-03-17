<properties
	pageTitle="Generate and transfer HSM-protected keys"
	description="Generate and transfer HSM-protected keys"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="sudbalas"
	displayOrder="3"
	selfHelpType="generic"
	supportTopicIds="32596884"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-howtransferhsmkeys"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Generate and transfer HSM-protected keys
## **Recommended Steps**

* [Azure Key Vault HSM Pricing](https://azure.microsoft.com/pricing/details/key-vault/)
* [Azure Key Vault HSM Quota Limits](https://docs.microsoft.com/azure/key-vault/general/service-limits)
* [How to generate and transfer HSM-protected keys](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)

### **Troubleshooting**

* You must have an Azure Key Vault Premium SKU to create and store HSM keys. To change the SKU of your Key Vault see the following link. [Change Key Vault SKU](https://azidentity.azurewebsites.net/post/2018/08/03/azure-key-vault-upgrade-the-sku-of-your-key-vault)

* If you get any of the following errors, Unauthorized access, access denied, forbidden, the service principal used doesn't have access to the resource it's trying to access. 
Please see the key vault authentication document to resolve this issue. [Key Vault Authentication](https://docs.microsoft.com/azure/key-vault/general/authentication)

## **Recommended Documents**

* [Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)
