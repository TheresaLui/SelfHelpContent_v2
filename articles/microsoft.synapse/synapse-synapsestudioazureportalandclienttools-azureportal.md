<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738760"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Synapse Studio, Azure Portal and Client Tools/Azure Portal"
	description = "Synapse Studio, Azure Portal and Client Tools/Azure Portal"
	articleId = "synapse-synapsestudioazureportalandclienttools-azureportal"
	authors = "saltug"
	ms.author = "saltug"
/>

# Synapse Studio, Azure Portal and Client Tools/Azure Portal

### Known issues

* If there is a paused SQL Pool instance in a workspace when the "Grant CONTROL" setting is changed in the "Managed Identities" blade of the Synapse Workspace resource in the portal, the task does not complete. As a result the setting might not be applied on the SQL pool. In this situation in order to manually change the state of the setting in the SQL Pool:

	1. Click on "Launch Synapse Studio" in the portal
	2. Click Data in the Left Navigation Panel and navigate to the SQL Pool that needs the setting in the Databases section
	3. Invoke a "New SQL Script" on the SQL Pool 

	a. To create a new workspace managed identity user and to assign control permissions to the user run the following in the pool:<br>
	```CREATE USER [WorkspaceName] FROM EXTERNAL PROVIDER```<br>
	```GRANT CONTROL TO [WorkspaceName]```

	b. To revoke control on the SQL Pool (Note that Synapse orchestration scenarios will not work if this is run on this SQL Pool)<br>
	```REVOKE CONTROL TO [WorkspaceName]```

	c. To drop Workspace managed identity user (Note that Synapse orchestration scenarios will not work if this is run on this SQL Pool)<br>
	```DROP USER [WorkspaceName]```

* Creation of a new SQL pool operation might appear to have failed if your workspace name starts with a number. However, SQL pool is created successfully, the GRANT control setting would not have been applied correctly in this scenario. You need to follow the above steps to have the proper "Grant CONTROL" setting applied manually to your newly created SQL pools.

* If you have multiple AAD logins that is cached to your browser, opening Synapse Studio from Portal might not complete as your browser might try to use a different AAD account to authenticate you to Synapse Studio system. You might need to log off (or remove) other AAD account that is cached to your browser to complete your login to Synapse Studio.


## **Recommended Documents**

* [Create an Azure Synapse Analytics workspace](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-workspace)
* [Create a Synapse SQL pool](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-sql-pool)
* [Create Apache Spark pool using Azure portal](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-apache-spark-pool)
* [Delete Apache Spark pool](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-apache-spark-pool#clean-up-resources)
