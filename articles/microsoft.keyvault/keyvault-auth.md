<properties
  pagetitle="Azure Key Vault Authentication&#xD;"
  service="microsoft.keyvault"
  resource="vaults"
  ms.author="sudbalas,sebansal"
  selfhelptype="Generic"
  supporttopicids="32596880"
  resourcetags="optional"
  productpesids="15657"
  cloudenvironments="blackforest,fairfax,public,mooncake,usnat,ussec"
  articleid="keyvault-auth"
  ownershipid="AzureKeyVault_KeyVault" />
# Azure Key Vault Authentication

## **Recommended Steps**

Authentication with Key Vault works in conjunction with Azure Active Directory (AAD), which is responsible for authenticating the identity of any given security principal. You can authenticate to Key Vault with managed identity, service principal, or user principal.

* See [How Key Vault Authentication works](https://docs.microsoft.com/azure/key-vault/general/authentication-fundamentals).

### **Troubleshooting**

* **Unauthorized access, access denied, forbidden, or similar error**:  The principal used doesn't have access to the resource that it's trying to access. Grant the App Service's access to a resource.

* **Unable to authenticate using security groups**: Security groups in AAD can take up to 8 hours to propagate.

## **Recommended Documents**

* [Key Vault authentication troubleshooting guide](https://docs.microsoft.com/azure/key-vault/general/troubleshooting-access-issues)
* [Grant access to Key Vault with Access Policies](https://docs.microsoft.com/azure/key-vault/general/assign-access-policy-portal)
* [Grant access to Key Vault with Azure Roles](https://docs.microsoft.com/azure/key-vault/general/rbac-guide)
