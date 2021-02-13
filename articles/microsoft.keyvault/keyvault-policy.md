<properties
	pageTitle="Azure Key Vault Policy"
	description="Azure Key Vault Policy"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32783174"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-policy"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Policy For Azure Key Vault

## **Recommended Steps**

Azure Policy for Key Vault is a governance tool designed to help you manage your key vaults at scale.

* [Integrate Azure Key Vault with Azure Policy](https://docs.microsoft.com/azure/key-vault/general/azure-policy?tabs=certificates)

### **Troubleshooting**

* User can't create a policy definition:
    1. Dataplane policy for Key Vault is still in preview. **Custom policy definitions are not supported at this time.**
    1. For other policies, use a JSON validator, such as JSON Lint, to confirm the policy is valid JSON.
    1. You may be using a policy alias that is not supported. Run this command to get the updated list of supported aliases: `Get-AzPolicyAlias -NamespaceMatch ‘Microsoft.KeyVault’ -ListAvailable`

* The Deny policy is not taking effect:
    1. It may take up to 1 hour after policy assignment for the deny effect to start working.
    1. Make sure that enforcement is set to **Enabled** and effect is set to **Deny**. Both conditions need to be set.

* Audit policy is not showing results:
    1. Audit results may stay in the **Not Started** state or **0 out of 0** state for up to 24 hours after policy assignment.
