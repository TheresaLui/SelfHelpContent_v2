<properties
  pagetitle="Azure Pipelines issues related to repository integrations&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="vijayma,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742315"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesrepoissues"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines issues related to repository integrations

Most users could resolve issues relates to repository integrations by using the following information.

## **Recommended Steps**

Your source code may be in an Azure Repos, GitHub, BitBucket, or Subversion. Select the appropriate problem and the repository type below:

Follow through all the steps before you create a support ticket. If you need to create a ticket after completing the diagnostic steps, provide information about the path you took and results of the steps that you ran in your ticket to expedite the resolution of your issue.

* My repository is behind a firewall. How do I configure Azure Pipelines or hosted agents?

	- See [GitHub Enterprise](https://docs.microsoft.com/azure/devops/pipelines/repos/github-enterprise)
	- See [BitBucket server](https://docs.microsoft.com/azure/devops/pipelines/repos/on-premises-bitbucket)
	- See [Subversion](https://docs.microsoft.com/azure/devops/pipelines/repos/subversion)

* My pipeline is not being triggered when I make an update to the source code

	- Go back and change the problem type, as follows:
		* Problem type: **Pipelines - Building and testing your application**
		* Problem subtype: **CI, PR, or scheduled triggers**
	
* My pipeline is triggered, but it is **stuck waiting**

	- Go back and change the problem type as follows:
		* Problem type: **Pipelines - Configuring pipelines**
		* Problem subtype: **My pipelines are stuck waiting in a queue**

* I get an error in my "Check out" or "Get sources" step

	- Go back and change the problem type as follows:
		* Problem type: **Pipelines - Building and testing your application**
		* Problem subtype: **Getting source code from repository into pipeline**

* I have **other issues** with integrating my pipeline with Azure Repos, GitHub, BitBucket, or Subversion.

	- [Integrate with Azure repos](https://docs.microsoft.com/azure/devops/pipelines/repos/azure-repos-git?view=azure-devops)
	- [Integrate with GitHub repos](https://docs.microsoft.com/azure/devops/pipelines/repos/github?view=azure-devops)
	- [Integrate with GitHub Enterprise repos](https://docs.microsoft.com/azure/devops/pipelines/repos/github-enterprise?view=azure-devops)
	- [Integrate with BitBucket Cloud repos](https://docs.microsoft.com/azure/devops/pipelines/repos/bitbucket?view=azure-devops)
	- [Integrate with on-prem BitBucket repos](https://docs.microsoft.com/azure/devops/pipelines/repos/on-premises-bitbucket?view=azure-devops)
	- [Integrate with TFVC repos](https://docs.microsoft.com/azure/devops/pipelines/repos/tfvc?view=azure-devops)
	- [Integrate with Subversion repos](https://docs.microsoft.com/azure/devops/pipelines/repos/subversion?view=azure-devops)

## **Recommended Documents**

* [Checkout from multiple repos](https://docs.microsoft.com/azure/devops/pipelines/repos/multi-repo-checkout?view=azure-devops)
* [Run Git commands in a script](https://docs.microsoft.com/azure/devops/pipelines/scripts/git-commands?view=azure-devops&tabs=yaml)
* [Build Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
