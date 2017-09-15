<properties
	pageTitle="Changing Key Vault Type for Azure Key Vault"
	description="Changing Key Vault Type for Azure Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32375286"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Change Key Vault Type for Azure Key Vault
## **Recommended steps**

* There are two different types of Key Vaults: "Premium" and "Standard". Here is an example of how to create a "Premium" and "Standard" key vault, respectively. One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys. Assume that your vault name is "myvault".<br>
* Azure CLI 2.0:<br>
    ```
		az keyvault create --name 'myvault' --resource-group 'yourResourceGroup' --location 'East Asia' --sku 'Premium'
		az keyvault create --name 'myvault' --resource-group 'yourResourceGroup' --location 'East Asia' --sku 'Standard'
	```
* Azure PowerShell:<br>
	```
		New-AzureRmKeyVault -VaultName 'myvault' -ResourceGroupName 'yourResourceGroup' -Location 'East Asia' -SKU 'Premium'
		New-AzureRmKeyVault -VaultName 'myvault' -ResourceGroupName 'yourResourceGroup' -Location 'East Asia' -SKU 'Standard'
	```

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[How to Generate and Transfer HSM-protected Keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)