<properties
	pageTitle="How to Use Key Vault from Web Application"
	description="Using key vault from a web application"
	service="Microsoft.keyvault"
	resource="keyvault"
	authors="fhokholdMSFT"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32375291"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Use Key Vault from Web Application

## **Recommended steps**

* Use Key Vault from Web Application<br>

[Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)

* Before using from a web application you will need to have a key vault set up. This is how to create a key vault with a key and secret in it using Azure CLI 2.0.<br>

    ``` az login ```

    ``` az group create --name "ContosoResourceGroup" --location "East Asia" ```

    ``` az provider register --namespace Microsoft.KeyVault ```

    ``` az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete ```

    ``` az keyvault key create --vault-name 'testVault' --name 'ContosoFirstKey' --protection software ```

    ``` az keyvault secret set --vault-name 'testVault' --name 'SQLPassword' --value 'Pa$$w0rd' ```

    Next you need to [Register the application in Azure Active Directory](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)
    
    Then, authorize the Application to use secrets and keys.

    ``` az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --key-permissions decrypt sign ```

    ``` az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --secret-permissions get ```


## **Recommended documents**

[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)
