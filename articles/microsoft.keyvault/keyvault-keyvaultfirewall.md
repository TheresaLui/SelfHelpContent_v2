<properties
	pageTitle="Azure Key Vault Behind Firewall"
	description="Azure Key Vault Behind Firewall"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
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

* **Please note that while some Azure services are part of the trusted services list, they are only trusted for certain supported usage scenarios.** For example Azure App Service is only a trusted service for deploying web app certificates. Operations that are not part of supported usage scenarios will require that you add the resource's ip address or virtual ip address to the key vault firewall manually. Please see the links below for further guidance.

* **If you need to allow a service through the key vault firewall, please download the list of Azure IP Ranges and Service Tags.** The link is available below. Please click the download link from the Microsoft Download Center. You will get a json file that will provide IP addresses for specific azure services and regions. Enter the ip address ranges corresponding to your application and region into the key vault firewall allow list. 

* Azure key vault doesn't allow IP-based restrictions for private IP ranges. To restrict access to private IP ranges, you would need to use subnet rules.

## **Recommended Documents**

* [Azure IP Address Ranges and Service Tags - Public Cloud](https://www.microsoft.com/download/details.aspx?id=56519)<br>
* [Azure DevOps IP Address Ranges](https://docs.microsoft.com/azure/devops/organizations/security/allow-list-ip-url?view=azure-devops)<br>
* [Access Key Vault behind firewall](https://docs.microsoft.com/azure/key-vault/key-vault-access-behind-firewall)<br>
* [Virtual network service endpoints](https://docs.microsoft.com/azure/key-vault/key-vault-overview-vnet-service-endpoints)<br>
* [Configure firewalls and virtual networks](https://docs.microsoft.com/azure/key-vault/key-vault-network-security)<br>
* [Key Vault Trusted Services List](https://docs.microsoft.com/azure/key-vault/general/overview-vnet-service-endpoints#trusted-services)<br>
