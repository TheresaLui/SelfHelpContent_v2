<properties
	pageTitle="Key Vault Integrate with App Services"
	description="Key Vault Integrate with App Services"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32739887"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="sudbalas-keyvaultintegratewithappservices"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Integrate Azure Key Vault with App Services

## **Recommended Steps**

* **If your App Service cannot access Key Vault due to a firewall issue, please read the following guidance:**

Azure App Services is a Key Vault trusted service **only** for the scenario of deploying a certificate. All other operations in Azure App Service do not qualify as a Key Vault trusted service. To resolve this issue, you must grant your App Service access through the Key Vault Firewall by performing the following steps:

  1. Navigate to your App Service resource in the Azure portal
  2. Click on "Properties" in the App Service settings
  3. Find the IP Address of your App Service
  4. Add this IP Address to the "Allow" list of the Key Vault Firewall

* [Troubleshooting Key Vault References for App Service and Azure Functions](https://docs.microsoft.com/azure/app-service/app-service-key-vault-references#troubleshooting-key-vault-references)

## **Recommended Documents**

* [Key Vault App Service Reference](https://docs.microsoft.com/azure/app-service/app-service-key-vault-references)
* [Use Key Vault from App Service with MSI](https://docs.microsoft.com/samples/azure-samples/app-service-msi-keyvault-dotnet/keyvault-msi-appservice-sample/)
* [Use App Service Certificate with Key Vault](https://azure.microsoft.com/blog/internals-of-app-service-certificate/)

