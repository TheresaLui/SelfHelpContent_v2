<properties
	pageTitle="Pipelines timeouts"
	description="Azure Pipelines issues related to timeouts"
	infoBubbleText="Azure Pipelines issues related to timeouts"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma"
	ms.author="vijayma"
	articleId="AZDevOpsPipelinesTimeoutIssues"
	supportTopicIds="32742331"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines Timeout Issues

## **Recommended Steps**

Are you facing one of these common problems?

* I purchased additional parallel jobs. However, my pipelines still timeout after 60 minutes.

	- By purchasing Microsoft-hosted parallel jobs, you can increase your timeouts up to 6 hours per job. The default timeout is still 60 minutes. 
	- To increase the timeout in YAML pipelines, specify [timeoutInMinutes](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=yaml#timeouts) property in the YAML file.
	- To increase the timeout in classic pipelines, specify the value of timeout in [Options tab](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=classic#timeouts).

* I have pipelines that run several hours. How do I configure Azure Pipelines to run these pipelines?

	- The maximum duration of each job in a pipeline is 6 hours on Microsoft-hosted agents if you build open source or public projects. It is also 6 hours if you purchased Microsoft-hosted parallel jobs. Otherwise, it is 60 minutes. To go from 60 minutes to 6 hours, you need to [purchase](https://docs.microsoft.com/azure/devops/pipelines/licensing/concurrent-jobs?view=azure-devops) Microsoft-hosted parallel jobs.
	- There is no way to run jobs longer than 6 hours on Microsoft-hosted agents.
	- You can use self-hosted agents to run longer jobs. There are no limits on how long jobs can run on self-hosted agents.
	- You can split your pipeline into multiple jobs, each of which take less than 6 hours, and still run the pipeline on Microsoft-hosted agents.

* What are all the places where I can configure timeouts for my build or YAML pipelines?

	- You can configure timeout for each [step](https://docs.microsoft.com/azure/devops/pipelines/process/tasks?view=azure-devops&tabs=yaml#controloptions) and for each [job](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=yaml#timeouts) in a pipeline.
	- The maximum duration for each job is dependent on whether you use self-hosted agents (no limits) or [Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/licensing/concurrent-jobs?view=azure-devops). In the case of latter, it is further dependent on whether you use free tier for private projects (60 minute limit) or paid tier/public projects (6 hours).

* My pipeline waits a long time for an agent to be allocated.

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Configuring pipelines**
		* Problem subtype: **My pipelines are stuck waiting in a queue**
  
* I get an error "We stopped hearing from agent Azure Pipelines 2. Verify the agent machine is running and has a healthy network connection."

	- Please go back and change the problem type as follows:
		* Problem type: **Pipelines - Configuring pipelines**
		* Problem subtype: **Microsoft-hosted agents - disk space, IP address range, etc**

* I deployed a self hosted build agent as limit exceeded beyond the free minutes specified. However, all my builds still fail.

	- The pipeline would be pointing to an Azure Pipeline agent. Change the agent pool to the self-hosted pool and it should work fine.

* How do I increase build timeout?

	- Change the **jobTimeoutInminutes** value by referring to this [document](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=yaml#timeouts)

* My build pipeline is timing out even after setting the **Build timeout in minutes** to 0.

	- This is because the the **jobTimeoutInMinutes** is set to 60 for the pipeline. Change the timeout in the **Agent Job settings** to 0.

## **Recommended Documents**

* [Job timeouts in classic build or YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=yaml#timeouts)
* [Task or step timeouts](https://docs.microsoft.com/azure/devops/pipelines/process/tasks?view=azure-devops&tabs=yaml#task-control-options)
* [Timeouts in deployment groups](https://docs.microsoft.com/azure/devops/pipelines/process/deployment-group-phases?view=azure-devops&tabs=yaml#timeouts)
* [Timeouts in approvals and checks](https://docs.microsoft.com/azure/devops/pipelines/process/approvals?view=azure-devops&tabs=check-pass)
* [Timeouts in classic releases](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-using-approvals?view=azure-devops)
* [Timeouts and disconnects](https://docs.microsoft.com/azure/devops/pipelines/process/runs?view=azure-devops#timeouts-and-disconnects)
* [Maximum job limits for Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/licensing/concurrent-jobs?view=azure-devops)
* [Timeouts in Classic editor](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=classic#timeouts)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)
