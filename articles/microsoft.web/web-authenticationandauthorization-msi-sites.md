<properties
  pagetitle="authentication and authorization/Managed Service Identity (MSI) Integration "
  description="authentication and authorization/Managed Service Identity (MSI) Integration"
  service="microsoft.web"
  resource="sites"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32608648"
  resourcetags=""
  productpesids="14748,16170,16333"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="6b71a02d-8af7-4491-ba12-aff37179c77e"
  ownershipid="Compute_AppService" />
# authentication and authorization/Managed Service Identity (MSI) Integration 

Managed Service Identities is a feature that gives an Azure resource an identity in Azure AD. After the identity is created, you can assign the identity to a role-based access control (RBAC). This is different than authenticating an incoming request to the Azure resource, where MSI is enabled. 

## **Recommended Steps**

**Problem**: Receiving the following error messages when trying to access **Azure Key Vault** using managed identity:
* "HTTP Status Code: Forbidden"
* "The user, group, or application xxxx doesn't have the secrets to get permissions for Key Vault xxxx"
* "innercode":{"code":"AccessDenied"}
 
**Resolution**: 
* From Azure portal, navigate to the Access Policies blade of Key Vault.
* Select **+ Add Access Policy**.
* Provide necessary permissions under **Secret permissions**.
* Select **service principal** as the App Service name (when using system managed identity) or the User identity (when using user managed identity).
 
**Problem**: Receiving the following error messages when trying to access **Azure Storage** using managed identity:
* "HTTP Status Code: Forbidden"
* `AuthorizationPermissionMismatch`
* "This request is not authorized to perform this operation using this permission"
 
**Resolution**: 
* From Azure portal, navigate to the **Access Control (IAM)** blade of storage account.
* Select **+ Add role assignment**.
* Choose the necessary storage-related permission, such as Storage Blob Data Contributor.
* Select **service principal** as App Service name (when using system managed identity) or User identity (when using user managed identity).
 
**Problem**: Receiving the following error messages when trying to access **Azure SQL** using managed identity:
* "Unable to connect to SQL. Exception : Login failed for user <token-identified principal>"
 
**Resolution**: 
* **You can add the identity to an Azure AD group, then grant SQL Database access to the Azure AD group instead of the identity. For example, the following commands add the managed identity of the app to a new group called `myAzureSQLDBAccessGroup`**:
 
    groupid=$(az ad group create --display-name myAzureSQLDBAccessGroup --mail-nickname myAzureSQLDBAccessGroup --query objectId --output tsv)
    msiobjectid=$(az webapp identity show --resource-group myResourceGroup --name <app-name> --query principalId --output tsv)
    az ad group member add --group $groupid --member-id $msiobjectid
    az ad group member list -g $groupid
 

**Problem**: Experiencing issues with managed identity because the managed identity endpoint is not reachable. 
Error message: "An unexpected error occured while fetching the AAD Token"
 
**Resolution**: Ensure that your app is able to reach the managed identity endpoint in that region. For example, for the West Europe region, the managed identity endpoint is https://westeurope.login.microsoft.com. If your webapp traffic is routed through a firewall device, ensure that you allow these endpoints in the firewall for outgoing traffic.

## **Recommended Documents**

* [Managed Identity for Azure App Services - Microsoft Tech Community](https://techcommunity.microsoft.com/t5/apps-on-azure/managed-identity-for-azure-app-services/ba-p/1711597)
* [Use managed identities for App Service and Azure Functions](https://docs.microsoft.com/azure/app-service/overview-managed-identity) <br>
* [Managed identities for Azure resources](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview) <br>
* [Use managed identities (MSI) with an Azure App Service or an Azure Function](https://blogs.msdn.microsoft.com/benjaminperkins/2018/06/13/using-managed-service-identity-msi-with-and-azure-app-service-or-an-azure-function/) <br>
* [Azure services that support managed identity authentication](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/services-support-msi#azure-services-that-support-azure-ad-authentication) <br>
* [Azure services that support managed identity for Azure resources](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/services-support-msi#azure-services-that-support-managed-identities-for-azure-resources) <br>
* [Authentication and authorization in Azure App Service](https://docs.microsoft.com/azure/app-service/overview-authentication-authorization)<br>
* [Authentication and authorization error codes, ex: AADSTS####](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes)
