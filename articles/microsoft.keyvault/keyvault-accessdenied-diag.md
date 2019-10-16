<properties
	pageTitle="Access Denied Exception"
	description="Access Denied Exception"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="14"
	selfHelpType="diagnostics"
	supportTopicIds="32375285,32596881,32596883,32596883,32375288"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake"
	articleId="a0b57fdd-c29c-4a60-8b54-7a78da171846"
/>

# Access Denied Exception
## **Recommended Steps**

1. Check if there is access granted to key vault by looking in Key Vault Access Policies.
2. Grant access to Key Vault using MSI or Service Principal

## **Recommended Documents**

* [Provide Key Vault authentication with access control policy](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)<br>
* [Provice Key Vault authentication with managed identity](https://docs.microsoft.com/en-us/azure/key-vault/managed-identity)<br>
