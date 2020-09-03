<properties
	pageTitle="Azure SQL Database & SQL Server"
	description="Issues with building database, SSIS, or SSRS projects, or running SQL utilities and scripts in a pipeline"
	infoBubbleText="Azure Pipelines issues related to SQL projects and utilities"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsPipelinesAzureSQLIssues"
	supportTopicIds="32742307"
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

* I'm unable to build EF Migration leveraging manged identity

	[Follow the steps outlined in this document](https://docs.microsoft.com/en-us/azure/app-service/app-service-web-tutorial-connect-msi)

* I want to publish a .dacpac file
	The .dacpac file generated can be published by following the [given steps](https://docs.microsoft.com/en-us/azure/devops/pipelines/targets/azure-sqldb?view=azure-devops&tabs=classic#publish)

* How do I test & deploy SSIS

    [Follow these steps](https://docs.microsoft.com/en-us/sql/integration-services/devops/ssis-devops-overview?view=sql-server-ver15&viewFallbackFrom=sql-server-ver15%20https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Farchive%2Fmsdn-magazine%2F2013%2Faugust%2Fsql-server-unit-and-integration-testing-of-ssis-packages)

* Where do I find a sample to deploy to Azure SQL database

    You can refer this [tutorial](https://docs.microsoft.com/en-us/azure/devops-project/azure-devops-project-sql-database)


## **Recommended Documents**

* [Automate Build and Deployment of Azure SQL Database](https://docs.microsoft.com/en-us/archive/blogs/ssdt/sqldb-cicd-intro)
* [Azure SQL Managed Instance](https://docs.microsoft.com/en-us/azure/azure-sql/managed-instance/sql-managed-instance-paas-overview)
* [Deploy Integration Services (SSIS) Projects and Packages](https://docs.microsoft.com/en-us/sql/integration-services/packages/deploy-integration-services-ssis-projects-and-packages?view=sql-server-ver15)
* [SSIS DevOps Tools](https://docs.microsoft.com/en-us/sql/integration-services/devops/ssis-devops-overview?view=sql-server-ver15)