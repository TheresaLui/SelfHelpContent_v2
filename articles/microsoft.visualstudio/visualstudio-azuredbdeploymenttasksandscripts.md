<properties
	pageTitle="Azure database deployment tasks and scripts"
	description="Issues related to script deployment, configuration in the task or any guidance with the usage of the task"
	infoBubbleText="Azure Pipelines issues related to SQL script deployment and configuration"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AzureSQLIssues"
	supportTopicIds="32742294"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Azure SQL Database and Server

## **Recommended Steps**

Are you facing one of these common problems?

**I wasn't able to deploy DACPAC using the *DacpacTask* from Azure DevOps**

    The [DACPAC task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/sql-azure-dacpac-deployment?view=azure-devops) doesn't support service principle authentication. For [AAD authentication](https://docs.microsoft.com/archive/blogs/stefan_stranger/connect-to-azure-sql-database-by-obtaining-a-token-from-azure-active-directory-aad), execute the script using Azure PowerShell or PowerShell task. AAD-Integrated auth is  agent.

**SQL Package build failed**

    Ensure the dacpac file is present in your repository which is used for the build.

**How do I implement CI/CD for data factory in Azure DevOps**

    [Refer to this document to create an Azure Data Factory and implementing CI/CD for the same](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal).

**Where do I find a sample to deploy to Azure SQL database**

    You can refer this [tutorial](https://docs.microsoft.com/azure/devops-project/azure-devops-project-sql-database).


## **Recommended Documents**

* [Azure SQL database deployment](https://docs.microsoft.com/azure/devops/pipelines/targets/azure-sqldb?view=azure-devops&tabs=yaml)
* [Quickstart: Create a data factory by using the Azure Data Factory UI](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal)
* [DACPAC task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/sql-azure-dacpac-deployment?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
