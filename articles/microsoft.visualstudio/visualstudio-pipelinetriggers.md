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

3 out of every 5 problems related to triggering were solved by going through each of the solutions below.

## **Recommended Steps**

Your source code may be in an Azure Repos, GitHub, BitBucket, or SVN. You may be having trouble with CI, PR, CD, or pipeline-to-pipeline triggers.

Select the problem you are experiencing, and then select the repository type to see the detailed diagnostic steps. Follow through all the steps before you create a support ticket. Provide information about the results of each of the steps when you create a support ticket to expedite the resolution of your problem.

* I am setting up CI or PR triggers in my YAML pipeline, and they do not work. Updates to code do not start a new pipeline run.

	- Azure Repos Git repo: 
	- GitHub: 
	- GitHub Enterprise:
	- BitBucket Cloud:
	- BitBucket server:
	- SVN:
	- TFVC:

	
* I use **self-hosted agents** and my pipelines are stuck waiting in a queue although I see that all my agents are idle

	- Ensure that you haven't exceeded the [parallel job limits](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting/troubleshooting?view=azure-devops#my-pipeline-tries-to-start-but-never-gets-an-agent)
	- Ensure that your jobs aren't waiting for [approval](https://docs.microsoft.com/azure/devops/pipelines/process/approvals?view=azure-devops&tabs=check-pass)
	- Check the [agent pools](https://docs.microsoft.com/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml%2Cbrowser) page to see if all of your available agents are in use. 
	- Check if your pipeline has demands that don't match the capabilities of any of your agents. If only some of your agents have the desired capabilities and they are currently running other pipelines, your pipeline will be stalled until one of those agents becomes available. To check the capabilities and demands specified for your agents and pipelines, see [Capabilities](https://docs.microsoft.com/azure/devops/pipelines/agents/agents?view=azure-devops#capabilities).
	- Check the [Azure DevOps status page](https://status.dev.azure.com/) to ensure there aren’t any ongoing or past incidents in Azure Pipelines.

* I need to buy more concurrency or parallel jobs

	- Follow the [instructions here](https://docs.microsoft.com/azure/devops/organizations/billing/buy-more-build-vs?view=azure-devops) to purchase additional parallel jobs for private projects
	- If you maintain an open-source project, then continue and create a new support ticket to get additional free concurrency

## **Recommended Documents**

* [Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops)
* [Build Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting?view=azure-devops)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)
