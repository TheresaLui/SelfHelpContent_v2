<properties
	pageTitle="Azure Pipelines licensing and parallel jobs"
	description="Azure Pipelines issues related to licensing and parallel jobs"
	infoBubbleText="Azure Pipelines issues related to licensing and parallel jobs"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma"
	ms.author="vijayma"
	articleId="AZDevOpsPipelinesLicensing"
	supportTopicIds="32742317"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines licensing and parallel jobs issues

4 out of every 5 cases on licensing and parallel jobs were resolved using the solutions listed below.

## **Recommended Steps**

Are you facing one of these common problems?

* I need to **buy more concurrency** or parallel jobs

	- Follow the [instructions here](https://docs.microsoft.com/azure/devops/organizations/billing/buy-more-build-vs?view=azure-devops) to purchase additional parallel jobs for private projects
	- If you maintain an open-source project, then continue and create a new support ticket to get additional concurrency

* I wanted to run **two jobs** in parallel. So, I purchased an extra Microsoft-hosted parallel job on top of my free limit. However, I can still run only one job at a time.

	- Your first purchase removes the limits on your free allocation. It increases the number of minutes to unlimited and maximum time for each job to 6 hours. It does not give you a second parallel job on top of your free limit.
	- To be able to run two jobs in parallel, you need to buy two parallel jobs. See [Paying for parallel jobs](https://docs.microsoft.com/azure/devops/pipelines/licensing/concurrent-jobs?view=azure-devops) for more information.

* I purchased additional parallel jobs but my jobs still **timeout** after 60 minutes

	- By purchasing Microsoft-hosted parallel jobs, you can increase your timeouts up to 6 hours per job. The default timeout is still 60 minutes. 
	- To increase the timeout in YAML pipelines, specify [timeoutInMinutes](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=yaml#timeouts) property in the YAML file.
	- To increase the timeout in classic pipelines, specify the value of timeout in [Options tab](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=classic#timeouts).

* My pipelines are **stuck** waiting in a queue although I have a number of parallel jobs

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Configuring pipelines**
		* Problem subtype: **My pipelines are stuck waiting in a queue**

* I purchased additional parallel job but still have a problem with Microsoft-hosted agents

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Configuring pipelines**
		* Problem subtype: **Microsoft-hosted agents - disk space, IP address range, etc**

## **Recommended Documents**

* [Parallel jobs](https://docs.microsoft.com/azure/devops/pipelines/licensing/concurrent-jobs?view=azure-devops)
* [Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops)
* [Self-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/agents?view=azure-devops)
* [Azure DevOps Services Status](https://status.dev.azure.com)
