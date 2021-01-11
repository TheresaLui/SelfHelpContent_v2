<properties
  pagetitle="Azure pipelines issues while making use of Azure SQL Database and Server&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742307"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesazuresqlissues"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Azure SQL Database and Server

Resolve common pipeline issues with the following recommendations.

## **Recommended Steps**


* **I'm unable to build EF Migration leveraging managed identity**

   [Follow the steps outlined in this document](https://docs.microsoft.com/azure/app-service/app-service-web-tutorial-connect-msi)

* **I want to publish a .dacpac file**

   Publish the generated .dacpac file by following [these steps](https://docs.microsoft.com/azure/devops/pipelines/targets/azure-sqldb?view=azure-devops&tabs=classic#publish)

* **How do I test & deploy SSIS?**

   [Follow these steps](https://docs.microsoft.com/sql/integration-services/devops/ssis-devops-overview?view=sql-server-ver15&viewFallbackFrom=sql-server-ver15%20https%3A%2F%2Fdocs.microsoft.com%2F%2Farchive%2Fmsdn-magazine%2F2013%2Faugust%2Fsql-server-unit-and-integration-testing-of-ssis-packages)

* **Where do I find a sample to deploy to Azure SQL database?**

   Refer to this [tutorial](https://docs.microsoft.com/azure/devops-project/azure-devops-project-sql-database)

## **Recommended Documents**

* [Automate build and deployment of Azure SQL Database](https://docs.microsoft.com/archive/blogs/ssdt/sqldb-cicd-intro)
* [Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/sql-managed-instance-paas-overview)
* [Deploy Integration Services (SSIS) projects and packages](https://docs.microsoft.com/sql/integration-services/packages/deploy-integration-services-ssis-projects-and-packages?view=sql-server-ver15)
* [SSIS DevOps tools](https://docs.microsoft.com/sql/integration-services/devops/ssis-devops-overview?view=sql-server-ver15)
* [Azure SQL database deployment task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/sql-azure-dacpac-deployment?view=azure-devops)
* [Azure Database for MySQL deployment task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-mysql-deployment?view=azure-devops)
* [MySQL Database Deployment on Machine Group task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/mysqldb-deployment?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
