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
1. Assign access policies [Grant access to Key Vault with Access Policies](https://docs.microsoft.com/azure/key-vault/general/assign-access-policy-portal)
1. Assign Azure roles [Grant access to Key Vault with Azure Roles](https://docs.microsoft.com/azure/key-vault/general/rbac-guide)

**Troubleshooting**

1.	**I have an Administrator role, but I can’t perform an operation on a key vault.** 
	* Although having an admin role will allow you to grant yourself access to perform operations, for security, these operations are not necessarily granted by default. 
	*  Go to your key vault in the Azure Portal and click on the Access Control (IAM) tab. 
	* Confirm that you have administrator, owner, or contributor permissions in the scope of this key vault by clicking “View my Access”.
	* Click on the Access Policies tab. 
	* Find your service principal in the list. 
	* Confirm that you have been granted access to the key, secret, or certificate option you are trying to perform. 

2.	**I granted access to a security group, but members still cannot perform an operation.**
	* Permissions for security groups can take up to 24 hours in the worst case to propagate to all users, though it usually completes sooner. If you need to grant immediate 	access, try adding the service principal manually by adding a new access policy for that service principal. The assignment will take effect immediately. 
	
3.	**I had access to perform an operation before, but it no longer works.**
	* Make sure that the permissions for your service principal and/or security principal have not been changed. 
	* Go to your key vault on the Azure Portal. 
	* Click on the Access Policies Tab. 
	* Find the service principal / security group and confirm the permissions assigned. 
	
4.	**I can’t find the service principal to add access.**
	* Confirm that the service principal has a role assignment to your subscription in AAD. 
	* Go to Azure Active Directory on the Azure Portal. 
	* Click the “Users” tab
	* Search for the user you are trying to add. 
	* Click the Azure Role Assignments tab.
	* Confirm the user has the appropriate role assignment in the scope of your subscription. 

## **Recommended Documents**

* [Azure Active Directory Security Groups](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
* [Understand Key Vault Authentication](https://docs.microsoft.com/azure/key-vault/general/authentication)<br>
* [Understand Key Vault Access Model](https://docs.microsoft.com/azure/key-vault/general/secure-your-key-vault)<br>
