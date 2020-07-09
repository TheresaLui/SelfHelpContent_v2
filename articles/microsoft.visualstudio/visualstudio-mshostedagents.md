<properties
	pageTitle="Microsoft-hosted agents"
	description="Azure Pipelines issues related to Microsoft-hosted agents"
	infoBubbleText="Azure Pipelines issues related to Microsoft-hosted agents"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma"
	ms.author="vijayma"
	articleId="AZDevOpsPipelinesMSHostedIssues"
	supportTopicIds="32742318"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines Microsoft-hosted agent issues

4 out of every 5 cases on Microsoft-hosted agents were resolved using the solutions listed below.

## **Recommended Steps**

Are you facing one of these common problems?

* My pipelines are stuck waiting in a queue although I see that all my agents are idle

	- Ensure that you haven't exceeded the [parallel job limits](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting/troubleshooting?view=azure-devops#my-pipeline-tries-to-start-but-never-gets-an-agent)
	- Ensure that your jobs aren't waiting for [approval](https://docs.microsoft.com/azure/devops/pipelines/process/approvals?view=azure-devops&tabs=check-pass)
	- Check the [agent pools](https://docs.microsoft.com/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml%2Cbrowser) page to see if all of your available agents are in use. 
	- Check the [Azure DevOps status page](https://status.dev.azure.com/) to ensure there aren’t any ongoing or past incidents in Azure Pipelines.
	- [Report a service outage](https://support.microsoft.com/supportrequestform/e5848d32-abfe-4091-dbde-43caa4d30d0f). This is more effective than creating a support ticket.

* I need to buy more concurrency or parallel jobs

	- Follow the [instructions here](https://docs.microsoft.com/azure/devops/organizations/billing/buy-more-build-vs?view=azure-devops) to purchase additional parallel jobs for private projects
	- If you maintain an open-source project, then continue and create a new support ticket to get additional free concurrency

* My pipeline fails with the error: **no space left on device**

	Microsoft-hosted agents only have 10 GB of disk space available for running your job. We **cannot** increase the free space available on Microsoft-hosted images. Read the topic on [Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops) and the [Q & A](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#q--a) at the end of that topic to understand what consumes this space, and what you can do to workaround this problem.

* My pipeline fails with the following error: 

	```
	The agent did not connect within the allotted time of 45 minutes
	The request was abandoned due to an infrastructure failure. Notification of assignment to an agent was never received.
	```

	This is an indication that the service is experiencing a problem. [Report a service outage](https://support.microsoft.com/supportrequestform/e5848d32-abfe-4091-dbde-43caa4d30d0f). This is more effective than creating a support ticket.

* The pipeline fails because Microsoft-hosted agents are **unable to reach resources in my company network**

	If your pipelines need access to internal resources (for example, repository), then you must either use self-hosted agents or whitelist the IP address range for Microsoft-hosted agents in your firewall. Read the topic on [IP address range](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#agent-ip-ranges) for instructions.

* My pipeline **works on self-hosted agents**, but fails on Microsoft-hosted agents

	This clearly indicates that the software installed on Microsoft-hosted agents is not the same as that on your self-hosted agents. Read the section on [software](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#software) and [Q & A](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#q--a) to understand what is exactly installed on Microsoft-hosted agents and what you need to do to request an update to that software.

* I don't see Azure Pipelines agent pool

	Azure Pipelines agent pool or Microsoft-hosted agents are only available in Azure DevOps. They are not available in Azure DevOps Server or in TFS server. If you are using Azure DevOps, and are still not seeing the Azure Pipelines agent pool, see this [Q & A](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#q--a) and read this document to understand [permissions on agent pools](https://docs.microsoft.com/azure/devops/pipelines/agents/pools-queues?view=azure-devops#security).

* I want to get a new tool or software installed on Microsoft-hosted agents

	Do not open a support ticket. First, read this [Q & A](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#q--a). If needed, create a new issue in our [GitHub repository](https://github.com/actions/virtual-environments).

* I want bigger machines for my builds

	See the [hardware](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#hardware) that we use to run Microsoft-hosted agents. We **cannot** honor requests for bigger machines. Please use [self-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/agents?view=azure-devops) or [scale-set agents](https://docs.microsoft.com/azure/devops/pipelines/agents/scale-set-agents?view=azure-devops#security).

* I still have a problem with Microsoft-hosted agents

	- [Hardware](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops&tabs=yaml#hardware), [Software](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops&tabs=yaml#software), and [Networking](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#agent-ip-ranges) of Microsoft-hosted agents
	- [Security](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#security)
	- [Limitations](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops#capabilities-and-limitations)
	- Continue and create a support ticket

## **Recommended Documents**

* [Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops)
* [Build Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting?view=azure-devops)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)
