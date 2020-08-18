<properties
	pageTitle="Permission denied Creating, Reading, or Cancelling jobs"
	description="When you attempt to perform an operation on the jobs in a workspace but you receive a permission denied (403 Forbidden) error"
	infoBubbleText="Permission Denied Error"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="mblouin"
	displayOrder=""
	articleId="quantum-permissions-dataplane"
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds=""
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public"
	ownershipId=""
/>

# Performing an operation on the jobs in a workspace yields a 'Permission Denied' (403 Forbidden) error code

Azure Quantum uses RBAC (role based access contorl) to manage access rights for users and entities. You may receive an error if your workspace's permissions are not configured correctly.

## **Recommended Steps**

1. If you are new to RBAC permissions, please start by reviewing the [general RBAC documenation](https://docs.microsoft.com/en-us/azure/role-based-access-control/)
2. Review the **Access control (IAM)** blade of your quantum workspace to see the existing access configuration
3. Ensure that you have the required permissions to complete the operation that you are trying to carry out
