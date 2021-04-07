<properties
  pagetitle="authentication and authorization/Managed Service Identity (MSI) Integration &#xD;"
  description="authentication and authorization/Managed Service Identity (MSI) Integration"
  service="microsoft.web"
  resource="sites"
  ms.author="benperk,shrahman"
  selfhelptype="Generic"
  supporttopicids="32608573"
  resourcetags=""
  productpesids="16072"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="c6d4d389-4914-41ef-95ca-4fb4db038566"
  ownershipid="Compute_AppService" />
# Authentication and authorization/Managed Service Identity (MSI) Integration 

Managed Service Identities (MSI) is a feature that gives an Azure resource an identity in Azure AD. After the identity is created, you can assign it to a RBAC. This is different than authenticating an incoming request to the Azure resource where managed service identity is enabled. 


## **Recommended Steps**
**Errors trying to access **Azure Key vault** using managed identity:**
* HTTP Status Code: Forbidden
* "The user, group or application 'xxxx' does not have secrets get permission on key vault 'xxxx'"
* `"innercode":{"code":"AccessDenied"}`
 
**Resolution**: 
1. Navigate to the **Access Policies** blade of key vault from the Azure portal
2. Select **+ Add Access Policy**
3. Provide necessary permissions under **Secret permissions**
4. Select **service principal** as App Service name (when using system managed identity) or User identity (when using user managed identity)
 
**Errors trying to access **Azure Storage** using managed identity:**
* HTTP Status Code: Forbidden
* `AuthorizationPermissionMismatch`
* "This request is not authorized to perform this operation using this permission"
 
**Resolution**: 
1. Navigate to **Access Control (IAM)** blade of storage account from the Azure portal.
2. Select **+ Add role assignment**
3. Choose the necessary storage related permission, such as Storage Blob Data Contributor
4. Select **service principal** as App Service name (when using system managed identity) or User identity (when using user managed identity)
 
**Errors trying to access Azure SQL using managed identity:**
* "Unable to connect to SQL. Exception : Login failed for user '<token-identified principal>'"
 
**Resolution**: 
* Add the identity to an **Azure AD group**, then grant SQL Database access to the Azure AD group instead of the identity. For example, the following commands add the managed identity of the app to a new group called "myAzureSQLDBAccessGroup".

   ```
    groupid=$(az ad group create --display-name myAzureSQLDBAccessGroup --mail-nickname myAzureSQLDBAccessGroup --query objectId --output tsv)
    msiobjectid=$(az webapp identity show --resource-group myResourceGroup --name <app-name> --query principalId --output tsv)
    az ad group member add --group $groupid --member-id $msiobjectid
    az ad group member list -g $groupid
   ```
 
**Issues with managed identity as the managed identity endpoint is not reachable**<br>
Error: "An unexpected error occured while fetching the AAD Token"
 
**Resolution**: Ensure that your app is able to reach the managed identity endpoint in that region. For example, for the West Europe region this will be https://westeurope.login.microsoft.com. If your webapp traffic is routed through a firewall device, ensure that you allow these endpoints in the firewall for outgoing traffic.

## **Recommended Documents**

* [Use managed identities for App Service and Azure Functions](https://docs.microsoft.com/azure/app-service/overview-managed-identity) <br>
* [Managed identities for Azure resources](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview) <br>
* [Using managed identities (MSI) with an Azure App Service or an Azure Function](https://blogs.msdn.microsoft.com/benjaminperkins/2018/06/13/using-managed-service-identity-msi-with-and-azure-app-service-or-an-azure-function/) <br>
* [Azure services that support managed identity authentication](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/services-support-msi#azure-services-that-support-azure-ad-authentication) <br>
* [Azure services that support managed identity for Azure resources](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/services-support-msi#azure-services-that-support-managed-identities-for-azure-resources) <br>
* [Authentication and authorization in Azure App Service](https://docs.microsoft.com/azure/app-service/overview-authentication-authorization)<br>
* [Authentication and authorization error codes, ex: AADSTS####](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes)
