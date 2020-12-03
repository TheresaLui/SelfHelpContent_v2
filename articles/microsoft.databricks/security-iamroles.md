<properties
	pageTitle="Diagnose and resolve issues with IAM Roles"
	description="Diagnose and resolve issues with IAM Roles"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677697"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1c73a71c-111f-4375-9bda-0937354a5055"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with IAM Roles

Non-admin users of the Azure Databricks workspace simultaneously became unable to access the workspace by clicking the "Launch Workspace" button in the Azure Portal. When they do so, they receive an error message stating that they need to have Contributor or Owner permissions (Azure RBAC) on the workspace resource. However, the Contributor and Owner RBAC roles grant Databricks admin permissions, which is not appropriate for non-admin users.
 
A regular Databricks platform update adds additional logic to be executed when the "Launch Workspace" button is clicked in the Azure Portal. Some of the new logic entails administrative initialization/reinitialization tasks. Accordingly, the ability to click the button was restricted to users with Write permissions on the workspace resource: Contributors and Owners.

## **Recommended Steps**

Non-admin users may still access the workspace by directly navigating to the workspace URL. For convenience, the workspace URL is displayed in the Azure Portal above and to the right of the "Launch Workspace" button.
 
* User provisioning and permissions configuration in Azure Databricks - **capabilities and best practices**:
    * You can [add a user](https://docs.microsoft.com/azure/databricks/administration-guide/users-groups/users) to (within) a Databricks workspace without having to grant them any Azure RBAC role on the workspace resource (in the Azure Portal).
    * [Azure AD Guest users](https://docs.microsoft.com/azure/active-directory/external-identities/add-users-administrator) may be added to a Databricks workspace.
    * Users can be automatically provisioned/deprovisioned in an Azure Databricks workspace by [setting up SCIM for Azure AD](https://docs.microsoft.com/azure/databricks/administration-guide/users-groups/scim/aad).
    * Azure Databricks exposes [access control lists (ACLs)](https://docs.microsoft.com/azure/databricks/security/access-control/) within native permission definitions for workspace objects (e.g. notebooks), clusters, pools, jobs, tables, etc. The access control features are disabled by default, but [may be enabled by a workspace admin](https://docs.microsoft.com/azure/databricks/administration-guide/access-control/).
    * Automatic SCIM provisioning can be combined with access controls by:
      1. Granting permissions to custom [Databricks groups](https://docs.microsoft.com/azure/databricks/administration-guide/users-groups/groups)
      2. Adding Azure AD users to eponymous Azure AD groups
      3. Syncing Azure AD to Databricks via SCIM

## **Recommended Documents**

* [Security and permissions: tips and troubleshooting](https://docs.microsoft.com/azure/databricks/kb/security/)
