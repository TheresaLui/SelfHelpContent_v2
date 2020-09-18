<properties
	pageTitle="Databricks Library Installation Issues"
	description="Databricks Library Installation Issues"
	service="microsoft.Databricks"
	resource="workspaces"
	authors="kywe665"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32612199"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ec64425b-b8a8-4051-bcb3-ba53f931ffa5"
	ownershipId="AzureData_AzureDatabricks"
/> 

# Azure Databricks Library Installation

## **Recommended steps**

- Make sure your library is attached to the cluster you are attempting to use it on by [following these instructions](https://docs.databricks.com/user-guide/libraries.html#attach-a-library-to-a-cluster)
- Make sure to lock the version of the library you are using to protect against a third party update introducing a breaking change.
- If your libraries are out of sync between the UI and the API, follow instructions in [this document](https://docs.databricks.com/user-guide/faq/library-install-uninstall.html)
- If you are using the CosmosDB-Spark Connector Library, you may experience a library conflict. [Refer to this solution](https://docs.databricks.com/user-guide/faq/cosmosdb-connector-lib-conf.html)


## **Recommended documents**

1. [Library Lifecycle](https://docs.databricks.com/user-guide/libraries.html) - How to create, update, delete, attach, move, view, etc
2. [Library common issues FAQ](https://docs.databricks.com/user-guide/faq/library-install-uninstall.html)
