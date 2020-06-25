<properties
	pageTitle="Problem acquiring token for managed identity"
	description="Problem acquiring token for managed identity"
	infoBubbleText="An issue was found with acquiring a token for a managed identity"
	service="microsoft.azureactivedirectory"
	resource="userassignedidentities"
	authors="janelmsft"
	ms.author="janelmsft"
	displayOrder="2"
	articleId="Problem-acquiring-token-for-managed-identity"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32690728"
	resourceTags=""
	productPesIds="16985"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureIdentity_Managed Identities"
/>

# Problem acquiring token for the managed identity

To troubleshoot issues related to acquiring a token for a managed identity, see the steps below:

## **Recommended Steps**

1. Verify that the resource has been given a Managed Identity. Either system-assigned managed identity has been enabled or a user-assigned managed identity has been added. 
2. For user-assigned, ensure you're requesting the token for the correct identity. Provide `client_id`, `object_id` or `mi_res_id` as part of your token request to the local endpoint.

## **Recommended Documents**

* [How to acquire access token for managed identities](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)
