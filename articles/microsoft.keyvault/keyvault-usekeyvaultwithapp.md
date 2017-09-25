<properties
	pageTitle="How to Use Key Vault with an Application"
	description="Using key vault with an Application"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds="32375282"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Use Key Vault with an Application
## **Recommended Steps**

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
> [!NOTE]
>* Currently, the new feature Managed Service Identity (MSI) is the easiest way to authenticate. Managed Service Identity (MSI) allows you to automatically provision AAD Identities. For further details please see the following link to the sample using [Key Vault with MSI in an application in .NET](https://github.com/Azure-Samples/app-service-msi-keyvault-dotnet/) and related [MSI with App Service and Functions tutorial](https://docs.microsoft.com/azure/app-service/app-service-managed-service-identity). 
* Next you need to [Register the application in Azure Active Directory](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* Then, authorize the Application to use secrets and keys.<br>
    ``` 
		az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --key-permissions decrypt sign
		az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --secret-permissions get 
	```
	
##Troublshooting

* How do I associate a certificate with an Azure AD application?<br>
	```
		$x509 = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
		$x509.Import("C:\data\KVWebApp.cer")
		$credValue = [System.Convert]::ToBase64String($x509.GetRawCertData())

		# If you used different dates for makecert then adjust these values
		$now = [System.DateTime]::Now
		$yearfromnow = $now.AddYears(1)

		$adapp = New-AzureRmADApplication -DisplayName "KVWebApp" -HomePage "http://kvwebapp" -IdentifierUris "http://kvwebapp" -CertValue $credValue -StartDate $now -EndDate $yearfromnow

		$sp = New-AzureRmADServicePrincipal -ApplicationId $adapp.ApplicationId

		Set-AzureRmKeyVaultAccessPolicy -VaultName 'contosokv' -ServicePrincipalName $sp.ServicePrincipalName -PermissionsToSecrets all -ResourceGroupName 'contosorg'

		# get the thumbprint to use in your app settings
		$x509.Thumbprint
	```
* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)<br>
[Key Vault Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)<br>
[Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)<br>