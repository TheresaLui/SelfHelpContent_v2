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

* If there is a paused SQL Pool instance exist for a workspace and you try to change "Grant CONTROL" setting "Managed Identities" blade of the Synapse Workspace resource in the portal, this task might not complete. 

	1. Click on "Launch Synapse Studio" in the portal. 
	2. Click Data in the Left Navigation Panel and navigate to the SQL Pool that needs the setting in the Databases section. 
	3. Invoke a "New SQL Script" on the SQL Pool 

		a. To create a new workspace managed identity user and to assign control permissions to the user run the following in the pool:<br>
			```CREATE USER <WorkspaceName> FROM EXTERNAL PROVIDER```<br>
			```GRANT CONTROL TO <WorkspaceName>```

		b. To revoke control on the SQL Pool (Note that Synapse orchestration scenarios will not work if this run on this SQL Pool)<br>
			```REVOKE CONTROL TO <WorkspaceName>```

		c. To drop Workspace managed identity user (Note that Synapse orchestration scenarios will not work if this run on this SQL Pool)<br>
			```DROP USER <WorkspaceName>```

* If you have multiple AAD logins that is cached to your browser, opening Synapse Studio from Portal might not complete as your browser might try to use a different AAD account to authenticate you to Synapse Studio system. You might need to log off (or remove) other AAD account that is cached to your browser to complete your login to Synapse Studio.


## **Recommended Documents**

* [Create an Azure Synapse Analytics workspace](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-workspace)
* [Create a Synapse SQL pool](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-sql-pool)
* [Create Apache Spark pool using Azure portal](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-apache-spark-pool)
* [Delete Apache Spark pool](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-apache-spark-pool#clean-up-resources)
