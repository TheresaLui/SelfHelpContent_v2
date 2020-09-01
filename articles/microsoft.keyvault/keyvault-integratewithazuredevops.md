<properties
	pageTitle="Key Vault Integrate with Azure DevOps"
	description="Key Vault Integrate with Azure DevOps"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32739889"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="sudbalas-keyvaultintegratewithazuredevops"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Integrate Azure Key Vault with Azure DevOps
## **Recommended Documents**

* [Fetch Secrets from Key Vault in DevOps Pipeline](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-key-vault?view=azure-devops)

### **Troubleshooting**

* I am getting a 401 error connecting to Key Vault from my DevOps Pipeline even after allowing "Trusted Microsoft Services"

    Azure DevOps is not a Key Vault trusted service. If you have enabled the Azure Key Vault Firewall, you must manually whitelist the Azure DevOps IP Address Ranges.

    [Azure DevOps IP Address Ranges](https://docs.microsoft.com/azure/devops/organizations/security/allow-list-ip-url?view=azure-devops)

    [Azure Key Vault Trusted Services List](https://docs.microsoft.com/azure/key-vault/general/overview-vnet-service-endpoints#trusted-services)

    [Configure Azure Key Vault Firewall](https://docs.microsoft.com/azure/key-vault/general/network-security)
