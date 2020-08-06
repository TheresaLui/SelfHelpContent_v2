<properties
	pageTitle="Azure Key Vault Behind Firewall"
	description="Azure Key Vault Behind Firewall"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32596879"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-keyvaultfirewall"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Azure Key Vault Behind Firewall

## **Recommended Steps**

* Please note that while some Azure services are part of the trusted services list, they are only trusted for certain supported usage scenarios
* For example Azure App Service is only a trusted service for deploying web app certificates
* Operations that are not part of supported usage scenarios will require that you add the resource's ip address or virtual ip address to the key vault firewall manually
* Please see the links below for further guidance

## **Recommended Documents**

* [Access Key Vault behind firewall](https://docs.microsoft.com/azure/key-vault/key-vault-access-behind-firewall)<br>
* [Virtual network service endpoints](https://docs.microsoft.com/azure/key-vault/key-vault-overview-vnet-service-endpoints)<br>
* [Configure firewalls and virtual networks](https://docs.microsoft.com/azure/key-vault/key-vault-network-security)<br>
* [Key Vault Trusted Services List](https://docs.microsoft.com/azure/key-vault/general/overview-vnet-service-endpoints#trusted-services)<br>

