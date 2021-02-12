<properties
  pagetitle="ASC/Importing-Exporting App Service Certificates"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="curibe,shrahman"
  selfhelptype="Generic"
  supporttopicids="32604395"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="4ad65834-59f8-4cc1-b1e3-4bdc840d6245"
  ownershipid="Compute_AppService" />
# ASC/Importing-Exporting App Service Certificates

## **Recommended Steps**

* **How to Import a certificate from Key Vault to WebApp?**

   See [these instructions](https://docs.microsoft.com/azure/app-service/configure-ssl-certificate#import-a-certificate-from-key-vault).

* **How to Export a certificate from Key Vault as pfx?**

   See [these instructions](https://azure.github.io/AppService/appservicecertificate/2019/03/19/DevTalk-App-Service-Certificate-sync-improvements-and-design.html)

* **How to Export a certificate from Key Vault as pfx using PowerShell?**
    See [these instructions](https://docs.microsoft.com/azure/app-service/configure-ssl-certificate#export-certificate)

* **What permissions are required on Key Vault for App Service Certificate?**

|Service Principal|Secret Permissions|Certificates| 
|--|--|--|
|Microsoft Azure App Service|Get|Get|
|Microsoft.Azure.CertificateRegistration|Get,List,Set,Delete|Get,List|

* **Can App Service Certificate be used for Application Gateway or any other services?**

   Yes, certificates can be purchased through the App Service, then exported and uploaded for use with Application Gateway or any other service.

* **I am getting the error "The parameter keyVaultCsmId has an invalid value." What does that mean?**

You probably have another certificate already in the WebSpace that has same certificate name, but was imported from a different Key Vault or Key Vault Secret. 
You can import the certificate by using a different certificate name, using the PowerShell script provided in this [blog](https://dotnetdevlife.wordpress.com/2019/08/21/add-certificate-to-azure-appservice-from-keyvault/).

* **I am getting this error "The parameter KeyVaultId & KeyVaultSecretName has an invalid value". What does that mean?**

 This error occurs if you try to import a certificate from Key Vault, using an existing certificate name, and this existing certificate is imported from a different Key Vault, or from the same Key Vault but with a different secret. You can import the certificate using a different certificate name, using the PowerShell script provided in this [blog](https://dotnetdevlife.wordpress.com/2019/08/21/add-certificate-to-azure-appservice-from-keyvault/)

* **When trying to import a cert from Azure Key Vault in Azure Portal, I am getting the error "A resource with the same name cannot be created in location ‘XXXX’. Please select a new resource name." What does that mean?**

When you try to import a cert from Azure Key Vault in the Azure portal, the certificate resource name is set to [Key Vault name]-[Key Vault Secret]. Currently, there is no option in the portal to choose the certificate name. If you would like to import same Key Vault Certificate to more than one AppServicePlan, which are in different WebSpaces but in the same Resource Group, you need to use CLI, ARM, or PowerShell scripts so that you can give an unique certificate resource name per Resource Group.

## Recommended documents:

[az keyvault certificate](https://docs.microsoft.com/cli/azure/keyvault/certificate?view=azure-cli-latest#az-keyvault-certificate-import)
[Import Key Vault Certificate (PowerShell)](https://dotnetdevlife.wordpress.com/2019/08/21/add-certificate-to-azure-appservice-from-keyvault/)
