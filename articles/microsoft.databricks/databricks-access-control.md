<properties
	pageTitle="Databricks Access Control"
	description="Databricks Access Control"
	service="microsoft.databricks"
	resource="clusters"
	authors="bprakash"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32612192"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
/>

# Azure Databricks Access Control

## **Recommended steps**
The following details explain how to set up access control in Azure Databricks.

1. Create a Premium SKU of Azure Databricks workspace through the [Azure portal](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-portal). Access Control feature is only available in premium SKU.
2. Launch the workspace and go to [Admin Console](https://docs.azuredatabricks.net/administration-guide/admin-settings/index.html#admin-console) to enable/disable access control at various levels - Workspace, Cluster, Job, Table.
3. By default, all users have access to all data stored in a cluster’s managed tables unless an administrator enables table access control for that cluster. 

## **Recommended documents**
1. [Azure Databricks Access Control](https://docs.azuredatabricks.net/administration-guide/admin-settings/index.html#manage-access-control)
2. [Azure Databricks deep dive into deployment, and security](https://www.youtube.com/watch?v=IbtVZaUvESQ&feature=youtu.be&t=714)
