<properties
	pageTitle="Azure Key Vault Access Policies"
	description="Azure Key Vault Access Policies"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32743815"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-accesspolicies"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Azure Key Vault Access Policies and Azure RBAC

## **Recommended Steps**

1. Use Azure individual identity or security group
1. Assign access policies: [Grant access to Key Vault with Access Policies](https://docs.microsoft.com/azure/key-vault/general/assign-access-policy-portal)
1. Assign Azure roles: [Grant access to Key Vault with Azure Roles](https://docs.microsoft.com/azure/key-vault/general/rbac-guide)

**Troubleshooting Steps**

**You have an Administrator role, but can’t perform an operation on a key vault.** 
* Navigate to your key vault in the Azure Portal and click in the Access Control tab.
* Confirm that you have sufficient permissions by clicking View my Access.
* Click the Access Policies tab.
* Confirm that your service principal has permissions for the operation you are trying to perform.

**You granted access to a security group, but members still cannot perform an operation.**
* Permissions for security groups can take up to 24 hours at most to propagate to all users, though it usually completes sooner. If you need to grant immediate access, try adding the service principal manually by adding a new access policy for that service principal. The assignment will take effect immediately.

**You had access to perform an operation before, but it no longer works.**
* Make sure that the permissions for your service principal and/or security principal have not been changed.
* Go to your key vault on the Azure Portal.
* Click on the Access Policies Tab.
* Find the service principal / security group and confirm the permissions assigned.

**You can’t find the service principal in the key vault IAM tab.**
* Confirm that the service principal has a role assignment to your key vault in Azure Active Directory.
* Navigate to Azure Active Directory in the portal.
* Click the Users tab.
* Search for the service principal you are looking for.
* Click the Role Assignments tab.
* Confirm that the user has a role assignment for your key vault.

## **Recommended Documents**

* [Azure Active Directory Security Groups](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
* [Understand Key Vault Authentication](https://docs.microsoft.com/azure/key-vault/general/authentication)<br>
* [Understand Key Vault Access Model](https://docs.microsoft.com/azure/key-vault/general/secure-your-key-vault)<br>
