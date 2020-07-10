<properties
	pageTitle="Pipeline triggers aren't working"
	description="Azure Pipelines issues related to triggers"
	infoBubbleText="Azure Pipelines issues related to triggers"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma"
	ms.author="vijayma"
	articleId="AZDevOpsPipelinesTriggerIssues"
	supportTopicIds="32742305"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues related to triggers

3 out of every 5 problems related to triggers were solved using the solutions below.

## **Recommended Steps**

Your source code may be in an Azure Repos, GitHub, BitBucket, or Subversion. You may be having trouble with CI, PR, CD, or pipeline-to-pipeline triggers. Select the appropriate problem and the repository type below:

Follow through all the steps before you create a support ticket. If you do need to create a ticket after completing the diagnostic steps, provide information about the path you took and results of the steps you ran in your ticket to expedite the resolution of your problem.

* I am setting up **CI (Continuous Integration) or PR (Pull Request) triggers** in my **YAML pipeline**, and they do not work

	- [Azure Repos Git repo](https://docs.microsoft.com/azure/devops/pipelines/repos/azure-repos-git#failing-triggers)
	- [GitHub](https://docs.microsoft.com/azure/devops/pipelines/repos/github#failing-triggers)
	- [GitHub Enterprise](https://docs.microsoft.com/azure/devops/pipelines/repos/github-enterprise#failing-triggers)
	- [BitBucket Cloud](https://docs.microsoft.com/azure/devops/pipelines/repos/bitbucket#failing-triggers)
	- [BitBucket server](https://docs.microsoft.com/azure/devops/pipelines/repos/on-premises-bitbucket#failing-triggers)
	- [TFVC](https://docs.microsoft.com/en-us/azure/devops/pipelines/repos/tfvc#ci-triggers)
	- [Subversion](https://docs.microsoft.com/azure/devops/pipelines/repos/subversion#failing-triggers)
	
* I am using **scheduled triggers** in my **YAML pipeline**, and the pipeline is not being triggered on schedule

	- Read the suggestions in [scheduled triggers FAQ](https://docs.microsoft.com/azure/devops/pipelines/process/scheduled-triggers#faq).

* I am using **pipeline resources** in my **YAML pipeline**, and the pipeline is not being triggered

	- Read the section on [pipeline triggers](https://docs.microsoft.com/azure/devops/pipelines/process/pipeline-triggers?tabs=yaml) to understand the limitations of this feature.

* I have a **classic build or release pipeline**, and triggers do not work

	- [Classic release pipeline triggers](https://docs.microsoft.com/azure/devops/pipelines/release/triggers)
	- [Build completion triggers](https://docs.microsoft.com/azure/devops/pipelines/process/pipeline-triggers?tabs=classic) in classic build pipelines

* My pipeline is triggered, but it is **stuck waiting**

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Configuring pipelines**
		* Problem subtype: **My pipelines are stuck waiting in a queue**

* My pipeline is triggered, but fails in `checkout` or `get sources` step

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Building and testing your application**
		* Problem subtype: **Getting source code from repository into pipeline**

* I have **other issues** with integrating my pipeline with Azure Repos, GitHub, BitBucket, or Subversion.

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Building and testing your application**
		* Problem subtype: **GitHub, BitBucket, SVN integration**

## **Recommended Documents**

* [Triggers for each type of repo](https://docs.microsoft.com/azure/devops/pipelines/build/triggers?view=azure-devops)
* [Scheduled triggers](https://docs.microsoft.com/azure/devops/pipelines/process/scheduled-triggers?view=azure-devops&tabs=yaml)
* [Pipeline completion triggers](https://docs.microsoft.com/azure/devops/pipelines/process/pipeline-triggers?view=azure-devops&tabs=yaml)
* [Classic release management triggers](https://docs.microsoft.com/azure/devops/pipelines/release/triggers?view=azure-devops)
* [YAML syntax for triggers](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema?view=azure-devops&tabs=schema%2Cparameter-schema#triggers)
* [Build Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting?view=azure-devops)
* [Azure DevOps Services Status](https://status.dev.azure.com)
