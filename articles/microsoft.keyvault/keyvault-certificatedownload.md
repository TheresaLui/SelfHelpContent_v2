<properties
	pageTitle="Downloading Certificate from Key Vault"
	description="Downloading Certificate from Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="sebansal"
	ms.author="sebansal"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds="32783173"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-certificatedownload"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Downloading Certificate from Key Vault

## **Recommended Steps**

* You can export stored certificates in Azure Key Vault by using the Azure CLI, Azure PowerShell, or the Azure portal. [How to export certificate from Key vault](https://docs.microsoft.com/azure/key-vault/certificates/how-to-export-certificate?tabs=azure-cli#export-stored-certificates)

### **Troubleshooting**

* You only require a certificate password when you import the certificate in the key vault. Key Vault doesn't save the associated password. **When you export the certificate, the password would be blank.**
	
* Unauthorized access, access denied, forbidden, or similar error: The principal used doesn't have access to the resource it's trying to access. [Certificate Access Controls](https://docs.microsoft.com/azure/key-vault/certificates/certificate-access-control)

* I have accidentally **deleted a certificate**. How can I recover it?
	
	[List, recover or purge soft-deleted certificates](https://docs.microsoft.com/azure/key-vault/general/key-vault-recovery?tabs=azure-portal#list-recover-or-purge-soft-deleted-secrets-keys-and-certificates)

## **Recommended Documents**

* [Composition of a certificate](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates#composition-of-a-certificate)
* [Monitor and manage certificate creation](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-scenarios)
