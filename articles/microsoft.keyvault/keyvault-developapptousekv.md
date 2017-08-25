<properties
	pageTitle="How to Use Key Vault with an Application"
	description="Using key vault with an Application"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32382911"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Use Key Vault with an Application
## **Recommended steps**

* Use Key Vault with an Application<br>
[Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)
* Before using from a web application you will need to have a key vault set up. This is how to create a key vault with a key and secret in it using Azure CLI 2.0.<br>
	```
        az login 
        az group create --name "ContosoResourceGroup" --location "East Asia" 
        az provider register --namespace Microsoft.KeyVault 
        az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete 
        az keyvault key create --vault-name 'testVault' --name 'ContosoFirstKey' --protection software 
        az keyvault secret set --vault-name 'testVault' --name 'SQLPassword' --value 'Pa$$w0rd' 
	```
* Next you need to [Register the application in Azure Active Directory](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)
* Then, authorize the Application to use secrets and keys.
    ``` 
		az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --key-permissions decrypt sign
    	az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --secret-permissions get 
	```
## **Recommended documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)<br>
[Key Vault Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)<br>
[Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)<br>
[Certificate Based Authentication with Java](https://github.com/Azure-Samples/key-vault-java-certificate-authentication)