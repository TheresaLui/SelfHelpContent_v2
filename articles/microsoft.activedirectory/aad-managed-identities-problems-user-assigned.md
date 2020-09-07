<properties
	pageTitle="Problem with user-assigned managed identity"
	description="Problem with user-assigned managed identity"
	infoBubbleText="An issue was found with a user assigned managed identity"
	service="microsoft.azureactivedirectory"
	resource="userassignedidentities"
	authors="janelmsft"
	ms.author="janelg"
	displayOrder="4"
	articleId="8ea5c15d-425b-4257-a671-4e42c88a3b62"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32690729"
	resourceTags=""
	productPesIds="16985"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureIdentity_Managed Identities"
/>

# Problem with user-assigned managed identity

For issues related to managing a user-assigned managed identity:

## **Recommended Steps**

If you are unable to create a user-assigned managed identity:

- Ensure that you have sufficient permissions. At minimum, you need to have been granted "Managed Identity Contributor" role assignment, in order to create/delete user-assigned managed identities.

If you are unable to add a user-assigned managed identity to a resource:

- Ensure that you have sufficient permission. At minimum, you need to have been granted "Managed Identity Operator" as well as write permissions over the resource.

If you are unable to create role assignments for the managed identity:

- Ensure that you have sufficient permissions to manage Azure RBAC role assignments. You either need to have been granted User Access Administrator or Owner permissions over the resource, that you want to grant access to. 

## **Recommended Documents**

* [How to create a user-assigned managed identity](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/how-to-manage-ua-identity-portal#create-a-user-assigned-managed-identity)
* [How to delete a user-assigned managed identity](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/how-to-manage-ua-identity-portal#delete-a-user-assigned-managed-identity)
* [How to list a user-assigned managed identity](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/how-to-manage-ua-identity-portal#list-user-assigned-managed-identities)
