<properties
	pageTitle="Diagnose and resolve issues with Databricks access control"
	description="Diagnose and resolve issues with Databricks access control"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677682"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6de9bb37-2c67-4555-b104-9304a2ff6641"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks access control

 All non-admin users of Azure Databricks workspace simultaneously became unable to access the workspace by clicking the "Launch Workspace" button in the Azure Portal. When they attempt to do so, they receive an error message stating that they need to have Contributor or Owner permissions (Azure RBAC) on the workspace resource. However, the Contributor and Owner RBAC roles grant Databricks admin permissions, which is not appropriate for non-admin users.
 
A regular Databricks platform update added additional logic to be executed when the "Launch Workspace" button is clicked in the Azure Portal. Some of the new logic entailed administrative initialization/reinitialization tasks. Accordingly, the ability to click the button was restricted to users with "write" permissions on the workspace resource: Contributors and Owners.

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
* [Secrets](https://docs.microsoft.com/azure/databricks/security/secrets/secrets)
* [Create an Azure Key Vault-backed secret scope](https://docs.microsoft.com/azure/databricks/security/secrets/secret-scopes#--create-an-azure-key-vault-backed-secret-scope)
* [Cannot Read Azure Databricks Objects Stored in DBFS Root Directory](https://docs.microsoft.com/azure/databricks/kb/dbfs/dbfs-root-permissions)
