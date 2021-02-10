<properties
	pageTitle="Azure DevOps Pipelines"
	description="Issues in build steps of your pipeline when using .NETCore tasks"
	infoBubbleText="Azure Pipelines issues related to build tasks in the pipeline"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsBuildIssues"
	supportTopicIds="32742319"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues when using various build tasks

## **Recommended Steps**

Resolve common problems related to Azure pipelines when using various build tasks using these steps.

### Error "NU1101: Unable to find package WindowsAzure.Storage. No packages exist with this id in source(s): Microsoft Visual Studio Offline Packages" in the dotnet build task

Add a **dotnet restore** step before the build step. This will complete the restore before the build and add the `--no-restore` argument to the build step.

### .NET Core task is failing in my pipelines

Ensure that you are using the right version of the task and that the packages for the project are compatible with the target Netcore framework that makes use of latest MSBuild.

### An error occurs while running dotnet run extract

Make sure that you are using a proper format while running `dotnet run extract`.

### Need guidance on using the **.NetCore** build tasks in my Azure Pipelines

Refer to [this document](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/dotnet-core?view=azure-devops)

## **Recommended Documents**

* [YAML schema reference](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema?view=azure-devops&tabs=schema%2Cparameter-schema)
* [Build, test, and deploy .NET Core apps](https://docs.microsoft.com/azure/devops/pipelines/ecosystems/dotnet-core?view=azure-devops)
* [.NET Core CLI task](https://docs.microsoft.com/azure/devops/pipelines/tasks/build/dotnet-core-cli?view=azure-devops)
* [Create a CI/CD pipeline for .NET with Azure DevOps Starter](https://docs.microsoft.com/azure/devops-project/azure-devops-project-aspnet-core)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
