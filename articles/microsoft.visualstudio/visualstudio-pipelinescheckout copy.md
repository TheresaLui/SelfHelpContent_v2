<properties
	pageTitle="Pipelines integration with various repos"
	description="Azure Pipelines issues related to repository integrations"
	infoBubbleText="Azure Pipelines issues related to repository integrations"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma"
	ms.author="vijayma"
	articleId="AZDevOpsPipelinesRepoIssues"
	supportTopicIds="32742315"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues related to repository integrations

4 out of every 5 problems related to triggers were solved using the solutions below.

## **Recommended Steps**

Your source code may be in an Azure Repos, GitHub, BitBucket, or SVN. Select the appropriate problem and the repository type below:

Follow through all the steps before you create a support ticket. If you do need to create a ticket after completing the diagnostic steps, provide information about the path you took and results of the steps you ran in your ticket to expedite the resolution of your problem.

* My repository is behind a firewall. How do I configure Azure Pipelines or hosted agents?

	- [GitHub Enterprise](https://docs.microsoft.com/azure/pipelines/repos/ghe)
	- [BitBucket server](https://docs.microsoft.com/azure/pipelines/repos/onprem-bitbucket)
	- [Subversion](https://docs.microsoft.com/en-us/azure/devops/pipelines/repos/svn)

* My pipeline is not being triggered when I make an update to the source code

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Building and testing your application**
		* Problem subtype: **CI, PR, or scheduled triggers**
	
* My pipeline is triggered, but it is **stuck waiting**

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Configuring pipelines**
		* Problem subtype: **My pipelines are stuck waiting in a queue**

* I get an error in my `checkout` or `get sources` step

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Building and testing your application**
		* Problem subtype: **Getting source code from repository into pipeline**

* I have **other issues** with integrating my pipeline with Azure Repos, GitHub, BitBucket, or SVN.

	- [Integrate with Azure repos](https://docs.microsoft.com/azure/devops/pipelines/repos/azure-repos-git?view=azure-devops)
	- [Integrate with GitHub repos](https://docs.microsoft.com/azure/devops/pipelines/repos/github?view=azure-devops)
	- [Integrate with GitHub Enterprise repos](https://docs.microsoft.com/azure/devops/pipelines/repos/ghe?view=azure-devops)
	- [Integrate with BitBucket Cloud repos](https://docs.microsoft.com/azure/devops/pipelines/repos/bitbucket?view=azure-devops)
	- [Integrate with on-prem BitBucket repos](https://docs.microsoft.com/azure/devops/pipelines/repos/onprem-bitbucket?view=azure-devops)
	- [Integrate with TFVC repos](https://docs.microsoft.com/azure/devops/pipelines/repos/tfvc?view=azure-devops)
	- [Integrate with Subversion repos](https://docs.microsoft.com/azure/devops/pipelines/repos/svn?view=azure-devops)

## **Recommended Documents**

* [Checkout from multiple repos](https://docs.microsoft.com/azure/devops/pipelines/repos/multi-repo-checkout?view=azure-devops)
* [Run Git commands in a script](https://docs.microsoft.com/azure/devops/pipelines/scripts/git-commands?view=azure-devops&tabs=yaml)