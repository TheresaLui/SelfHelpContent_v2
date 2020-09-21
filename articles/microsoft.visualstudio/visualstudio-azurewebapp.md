<properties
	pageTitle="Azure Web Apps or App Services"
	description="Azure Pipelines issues related to deploying to Azure Web Apps or App Services"
	infoBubbleText="Azure Pipelines issues related to deploying to Azure Web Apps or App Services"
	service="microsoft.visualstudio"
	resource="account"
	authors="ninallam"
	ms.author="ninallam"
	articleId="AZDevOpsPipelinesAzureWebAppIssues"
	supportTopicIds="32742304"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues deploying to Azure Web Apps or App Services

## **Recommended Steps**

Are you facing one of these common problems?

* I am seeing the error **No package found with specified pattern** in the task

	Check if the package mentioned in the task is published as an artifact in the build or a previous stage and downloaded in the current job.

* The task fails with **5xx error** code

	 If you are seeing a 5xx error, then check the status of your Azure service [here](https://status.azure.com/status)

* The task fails with the error: **Could not fetch access token for Azure. Verify if the Service Principal used is valid and not expired**

	 Verify validity of the service principal used and that it is present in the app registration. For more details, see [Use Role-Based Access Control to manage access to your Azure subscription resources.](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)

* I am seeing an **SSL error** in the App Service or Web App deploy task

	 To use a certificate in App Service, it must be signed by a trusted certificate authority. [Look here](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-deployment?view=azure-devops#ssl-error) to resolve this error.

* My task fails with error **Publish using zip deploy option is not supported for msBuild package type**

	Web packages created using MSBuild task (with default arguments) have a nested folder structure that can only be deployed correctly by Web Deploy. Publish to zip deploy option cannot be used to deploy those packages. To convert the packaging structure, [follow these steps](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-deployment?view=azure-devops#error-publish-using-zip-deploy-option-is-not-supported-for-msbuild-package-type).

* I am seeing a **Web Deploy Error** in the App Service deploy task

	If you are using web deploy to deploy your app, in some error scenarios Web Deploy will show an error code in the log. To troubleshoot a web deploy error see look [here](https://docs.microsoft.com/iis/publish/troubleshooting-web-deploy/web-deploy-error-codes).

* Web app deployment on Windows is successful but the app is not working

	This might be because web.config is not present in your app. [Follow these steps to add a web.config](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app?view=azure-devops#web-app-deployment-on-windows-is-successful-but-the-app-is-not-working)

* Web app deployment on **App Service Environment (ASE)** is not working

	[Follow these steps to ensure you are deploying correctly](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app?view=azure-devops#web-app-deployment-on-app-service-environment-ase-is-not-working)

* A release hangs for long time and then fails

	This may be because there is insufficient capacity on your App Service Plan. To resolve this, you can scale up the App Service instance to increase available CPU, RAM, and disk space or try with a different App Service plan.

* I need guidance on deploying an app to Azure Web App

	You can refer to tutorials on deploying apps of various languages to an Azure Web App
	- [Python to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops)
	- [PHP to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/php-webapp?view=azure-devops)
	- [Java to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/java-webapp?view=azure-devops&tabs=java-tomcat)
	- [JavaScript and Node.js to Web App](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/javascript?view=azure-devops&tabs=code)

## **Recommended Documents**

* [App Service Deploy task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-deployment?view=azure-devops#troubleshooting)
* [Azure Web App task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app?view=azure-devops#troubleshooting)
* [Azure Web Apps for Container task Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-rm-web-app-containers?view=azure-devops#troubleshooting)
* [Deploy to Linux Web App](https://docs.microsoft.com/azure/devops/pipelines/targets/webapp-linux?view=azure-devops&tabs=dotnet-core%2Cyaml)
* [Deploy to Windows Web App](https://docs.microsoft.com/azure/devops/pipelines/targets/webapp?view=azure-devops&tabs=yaml)
* [Deploy to Web App for Containers](https://docs.microsoft.com/azure/devops/pipelines/targets/webapp-on-container-linux?view=azure-devops&tabs=dotnet-core%2Cyaml)