<properties
	pageTitle="Responding to Azure Defender for Key Vault alerts"
	description="Responding to Azure Defender for Key Vault alerts"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="sebansal"
	ms.author="sebansal"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds="32783952"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-azuredefnderalerts"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Responding to Azure Defender for Key Vault alerts

## **Recommended Steps**

* When you receive an alert from Azure Defender for Key Vault, we recommend you to investigate the alert. Azure Defender for Key Vault protects applications and credentials, so even if you're familiar with the application or user that triggered the alert, it's important to verify the situation surrounding every alert. [How to respond to unusual alert](https://docs.microsoft.com/azure/security-center/defender-for-key-vault-usage)

* Familiarize yourself with the [types of alerts for Key Vault](https://docs.microsoft.com/azure/security-center/alerts-reference#alerts-azurekv)

### **Troubleshooting**

* Based on the type of access that occurred, some fields might not be available. For example, if your key vault was accessed by an application, you won't see an associated User Principal Name. If the traffic originated from outside of Azure, you won't see an Object ID.
	

## **Recommended Documents**

* [About Azure Defender for Key vault](https://techcommunity.microsoft.com/t5/azure-security-center/azure-defender-for-key-vault/ba-p/1825055)
* [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender)
