<properties
	pageTitle="How to Generate and Transfer HSM-protected Keys for Azure Key Vault"
	description="Importing a key from a HSM to Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32375292"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Generate and Transfer HSM-protected Keys for Azure Key Vault
## **Recommended Steps**

* How to import a key from a HSM<br>
[HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)
* Before importing a HSM-protected key to key vault you will need to download the BYOK toolset. Please note that is feature is available on Windows only<br>
* Generate a key using Thales generatekey program.<br>
	```
		generatekey --generate simple type=RSA size=2048 protect=module ident=contosokey plainname=contosokey nvram=no pubexp=
	```
* Transfer your key to your key vault.<br>
	```
        Add-AzureKeyVaultKey -VaultName 'ContosoKeyVaultHSM' -Name 'ContosoFirstHSMkey' -KeyFilePath 'c:\KeyTransferPackage-ContosoFirstHSMkey.byok' -Destination 'HSM'
	``` 

##Troublshooting

* How to Setup a Key Vault for HSM-protected Keys?<br>
* There are two different types of Key Vaults: "Premium" and "Standard". Here is an example of how to create a "Premium" and "Standard" key vault, respectively. One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys. Assume that your vault name is "myvault" and your resource group name is "yourResourceGroup".<br>
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
[How to Generate and Transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)