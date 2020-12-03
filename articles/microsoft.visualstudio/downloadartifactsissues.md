<properties
	pageTitle="Azure Artifacts"
	description="Issues with Download Build/Pipeline artifact tasks, or authenticating with Azure Artifacts feeds"
	infoBubbleText="Azure Pipelines issues related to Publish, Download artifacts in pipelines and azure artifacts"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsPipelinesAzureWebAppIssues"
	supportTopicIds="32742292"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of artifacts from both Azure Artifacts & Azure Pipelines

## **Recommended Steps**

Are you facing one of these common problems?

* I encounter an error **NU1101: Unable to find package WindowsAzure.Storage. No packages exist with this id in source(s): Microsoft Visual Studio Offline Packages** in the DotNet build task

	Add a **dotnet restore** step before the build step which will complete the restore before the build and add the **--no-restore** argument to the build step.


* Build jobs in Azure DevOps are failing to access Nuget Packages in Artifact feed. 

	 Ensure the **Allow project-scoped builds** option is enabled in the Artifact feed settings

* Within release pipelines, I no longer seem to be able to select a single artifact to download.

	This might be a UI issue. Try out in different browsers. In most cases, the options are misplaced and will be moved to the bottom of the page. 

* I'm facing an error with **dotnet pack** task

    [Follow these steps](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-pack)

* NuGet push task fails on lacking permissions
    
    In such scenarios, build identity will not have permissions on that feed. The default Contributor group '[team]\Project Collection Build Service Accounts' apparently does not include the 'Project Collection Build Service' as a member using the default settings. Adding the 'Project Collection Build Service' account directly fixes this issue.

* I would like to consume the generated artifacts from a specific build in another YAML pipeline

    Make use of the [Download Pipeline Artifacts task](https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/download-pipeline-artifact?view=azure-devops)

* I need guidance on using the Azure Artifacts in Azure Pipelines

	You can refer to tutorials for publishing & consuming Artifact feeds on the following packages
    - [NuGet](https://docs.microsoft.com/en-us/azure/devops/artifacts/get-started-nuget?view=azure-devops)
	- [npm](https://docs.microsoft.com/en-us/azure/devops/artifacts/get-started-npm?view=azure-devops&tabs=windows)
	- [maven](https://docs.microsoft.com/en-us/azure/devops/artifacts/get-started-maven?view=azure-devops)
	- [python](https://docs.microsoft.com/en-us/azure/devops/artifacts/quickstarts/python-packages?view=azure-devops)
	- [Universal Packages](https://docs.microsoft.com/en-us/azure/devops/artifacts/quickstarts/universal-packages?view=azure-devops&tabs=azuredevops)


## **Recommended Documents**

* [Project scoped feeds](https://docs.microsoft.com/en-us/azure/devops/artifacts/feeds/project-scoped-feeds?view=azure-devops)
* [Artifacts in Azure Pipelines](https://docs.microsoft.com/en-us/azure/devops/pipelines/artifacts/build-artifacts?view=azure-devops&tabs=yaml)
* [Publish and download artifacts in Azure Pipelines](https://docs.microsoft.com/en-us/azure/devops/pipelines/artifacts/pipeline-artifacts?view=azure-devops&tabs=yaml)
* [Release artifacts & Artifact sources](https://docs.microsoft.com/en-us/azure/devops/pipelines/release/artifacts?view=azure-devops#:~:text=A%20release%20is%20a%20collection,different%20types%20of%20artifact%20repositories.)
* [Restore NuGet packages in Azure Pieplines](https://docs.microsoft.com/en-us/azure/devops/pipelines/packages/nuget-restore?view=azure-devops)
