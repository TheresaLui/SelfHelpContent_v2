<properties
	pageTitle="Configuring an Application for Multi-Region Reduntant Operation"
	description="Configuring an Application for Multi-Region Reduntant Operation"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="17"
	selfHelpType="resource"
	supportTopicIds="32375287"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="MoonCake"
	articleId="cb727e8d-89ea-4d5e-ba1f-d1679f0ecb35"
/>

# How to configure an application for multi-region reduntant operation
## **Recommended steps**

* Key Vault features multiple layers of redundancy in order to maintain availability.

    [Availability and Redundancy Azure Key Vault](https://docs.azure.cn/key-vault/key-vault-disaster-recovery-guidance)

**Troublshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?

    [Change a key vault tenant ID after a subscription move](https://docs.azure.cn/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

    [Grant permission to many applications to access a key vault](https://docs.azure.cn/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Availability and Redundancy Azure Key Vault](https://docs.azure.cn/key-vault/key-vault-disaster-recovery-guidance)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)
* [Create and Manage using CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)