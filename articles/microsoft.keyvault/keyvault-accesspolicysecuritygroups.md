<properties
  pagetitle="Azure Key Vault Access Policies and Azure RBAC&#xD;"
  description="Azure Key Vault Access Policies"
  service="microsoft.keyvault"
  resource="vaults"
  ms.author="sudbalas,sebansal"
  selfhelptype="Generic"
  supporttopicids="32743815"
  resourcetags="optional"
  productpesids="15657"
  cloudenvironments="blackforest,fairfax,public,mooncake,usnat,ussec"
  articleid="keyvault-accesspolicies"
  ownershipid="AzureKeyVault_KeyVault" />
# Azure Key Vault Access Policies and Azure RBAC

## **Recommended Steps**

1. Use Azure individual identity or security group
2. Assign access policies: [Grant access to Key Vault with Access Policies](https://docs.microsoft.com/azure/key-vault/general/assign-access-policy-portal)
3. Provide access to Key Vault keys, certificates, and secrets with an Azure RBAC [Grant access to Key Vault with Azure Roles](https://docs.microsoft.com/azure/key-vault/general/rbac-guide)

### Troubleshooting Steps

**You have an Administrator role, but can’t perform an operation on a key vault** 
1. Navigate to your key vault in the Azure Portal and select the **Access Control** tab
2. Confirm that you have sufficient permissions by selecting **View my Access**
3. Select the **Access Policies** tab
4. Confirm that your service principal has permissions for the operation you are trying to perform

**You granted access to a security group, but members still cannot perform an operation**
* Permissions for security groups can take up to 24 hours at most to propagate to all users, though it usually completes sooner. If you need to grant immediate access, try adding the service principal manually by adding a new access policy for that service principal. The assignment will take effect immediately.

**You had access to perform an operation before, but it no longer works**
1. Make sure that the permissions for your service principal and/or security principal have not been changed
2. Go to your key vault on the Azure portal
3. Select the **Access Policies** tab
4. Find the service principal/security group and confirm the permissions assigned

**You can’t find the service principal in the key vault IAM tab**
1. Confirm that the service principal has a role assignment to your key vault in Azure Active Directory
2. Navigate to Azure Active Directory in the portal
3. Select the **Users** tab
4 Search for the service principal you're looking for, and select the **Role Assignments** tab
5. Confirm that the user has a role assignment for your key vault

## **Recommended Documents**

* [Azure Active Directory Security Groups](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
* [Understand Key Vault Authentication](https://docs.microsoft.com/azure/key-vault/general/authentication)<br>
* [Understand Key Vault Access Model](https://docs.microsoft.com/azure/key-vault/general/secure-your-key-vault)<br>
