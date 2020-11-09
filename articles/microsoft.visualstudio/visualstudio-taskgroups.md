<properties
	pageTitle="Task groups"
	description="Issues related to task group creation, usage, errors while using them in classic build or release pipelines"
	infoBubbleText="Azure Pipelines issues related to task groups"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsPipelineTaskGroupIssues"
	supportTopicIds="32742329"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while using Task groups

## **Recommended Steps**

Are you facing one of these common problems?

****

* **I want to pass the Resource Group name from the release pipeline to the task group**

    Use pipeline variable to pass the Resource Group value to the task group.

* **I'm unable to add Task Group to a deployment group job**

    In such cases, ensure that it is compatible with an agent and add a Deployment group to the **runsOn** parameter of the job.

* **My Task Groups are not working consistently and it fails with the *Error:Failed to connect to remote machine. Verify the SSH service connection details.***

    This is encountered if the agent job is mentioned as **Azure pipelines** for the release pipelines with the task group. In such scenarios, change it such that the pipeline makes use of the self-hosted agent that is configured.

* **I'm facing an issue with my task group which gives an *Error:Missing default value for the variable in Task Group definition.***

    Provide a default value for the variable in the task group definition. [Refer this document](https://docs.microsoft.com/azure/devops/pipelines/library/task-groups?view=azure-devops#before-you-create-a-task-group)


## **Recommended Documents**

* [Task groups for builds and releases](https://docs.microsoft.com/azure/devops/pipelines/library/task-groups?view=azure-devops)
* [Create a task group](https://docs.microsoft.com/azure/devops/pipelines/library/task-groups?view=azure-devops#create-a-task-group)
