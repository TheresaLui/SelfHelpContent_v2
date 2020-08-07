<properties
	pageTitle="Azure Function Apps"
	description="Azure Pipelines issues related to deploying to Azure Function Apps"
	infoBubbleText="Azure Pipelines issues related to deploying to Azure Function Apps"
	service="microsoft.visualstudio"
	resource="account"
	authors="ninallam"
	ms.author="ninallam"
	articleId="AZDevOpsPipelinesAzureWebAppIssues"
	supportTopicIds="32742297"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues deploying to Azure Function Apps

## **Recommended Steps**

Are you facing one of these common problems?

* I am seeing the error **No package found with specified pattern** in the task

	Check if the package mentioned in the task is published as an artifact in the build or a previous stage and downloaded in the current job.

* The task fails with **5xx error** code

	 If you are seeing a 5xx error, then check the status of your Azure service [here](https://status.azure.com/status)

* The task fails with the error: **Could not fetch access token for Azure. Verify if the Service Principal used is valid and not expired**

	 Verify validity of the service principal used and that it is present in the app registration. For more details, see [Use Role-Based Access Control to manage access to your Azure subscription resources.](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)

* I am seeing an **SSL error** in the Azure Function App deploy task

	 To use a certificate in App Service, it must be signed by a trusted certificate authority. [Look here](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-function-app?view=azure-devops#ssl-error) to resolve this error.

* Function app deployment on Windows is successful but the app is not working

	This might be because web.config is not present in your app. [Follow these steps to add a web.config](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-function-app?view=azure-devops#function-app-deployment-on-windows-is-successful-but-the-app-is-not-working)

* I need guidance on deploying an app to Azure Web App

	You can refer to tutorial on deploying an app to an Azure Function App
	- [Java to Function App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/java-function?view=azure-devops)

## **Recommended Documents**

* [Azure Function App task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-function-app?view=azure-devops#troubleshooting)
* [Azure Function App for Container task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-functionapp-containers?view=azure-devops#troubleshooting)
* [Deploy to Function App on Linux](https://docs.microsoft.com/azure/devops/pipelines/targets/azure-functions?view=azure-devops&tabs=dotnet-core%2Cyaml)
* [Deploy to Function App on Windows](https://docs.microsoft.com/azure/devops/pipelines/targets/azure-functions-windows?view=azure-devops&tabs=dotnet-core%2Cyaml)
* [Deploy to Function App for Containers](https://docs.microsoft.com/azure/devops/pipelines/targets/function-app-container?view=azure-devops&tabs=yaml)