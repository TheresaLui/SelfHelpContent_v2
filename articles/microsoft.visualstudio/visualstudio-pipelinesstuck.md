<properties
	pageTitle="Pipelines are stuck"
	description="Azure Pipelines issues related to pipelines being stuck waiting in a queue"
	infoBubbleText="Azure Pipelines issues related to pipelines being stuck waiting in a queue"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma"
	ms.author="vijayma"
	articleId="AZDevOpsPipelinesStuck"
	supportTopicIds="32742320,32742321"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines stuck waiting in a queue

3 out of every 5 cases related to pipelines being stuck waiting were resolved using the solutions listed below.

## **Recommended Steps**

Are you facing one of these common problems?

* I use **Microsoft-hosted agents** and my pipelines are stuck waiting in a queue although I see that all my agents are idle

	- Ensure that you haven't exceeded the [parallel job limits](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting/troubleshooting?view=azure-devops#my-pipeline-tries-to-start-but-never-gets-an-agent)
	- Ensure that your jobs aren't waiting for [approval](https://docs.microsoft.com/azure/devops/pipelines/process/approvals?view=azure-devops&tabs=check-pass)
	- Check the [agent pools](https://docs.microsoft.com/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml%2Cbrowser) page to see if all of your available agents are in use. 
	- Check the [Azure DevOps status page](https://status.dev.azure.com/) to ensure there aren’t any ongoing or past incidents in Azure Pipelines.
	- [Report a service outage](https://support.microsoft.com/supportrequestform/e5848d32-abfe-4091-dbde-43caa4d30d0f). This is more effective than creating a support ticket.

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
