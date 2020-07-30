<properties
	pageTitle="Azure File Copy task"
	description="Azure Pipelines issues related to deploying to Azure File Copy task"
	infoBubbleText="Azure Pipelines issues related to deploying to Azure File Copy task"
	service="microsoft.visualstudio"
	resource="account"
	authors="ninallam"
	ms.author="ninallam"
	articleId="AZDevOpsPipelinesAzureFileCopyIssues"
	supportTopicIds="32742296"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines issues related to Azure File Copy task

## **Recommended Steps**

Are you facing one of these common problems?

* Can I run the task on a Linux Agent?

	This task is written in PowerShell and thus works only when run on **Windows agents**. If your pipelines require Linux agents and need to copy files to an Azure Storage Account, consider running az storage blob commands in the [Azure CLI task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-cli?view=azure-devops) as an alternative.

* The task is failing due to **Authentication** issues

	 If you are using task version 4, the Service Principal would require more permissions for enhanced security. The following permissions need to be provided
	 * [Storage Blob Data Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor)
	 * [Storage Blob Data Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-data-owner)
	 For more details on the level of authorization [look here](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10#option-1-use-azure-active-directory)

* The task is not resuming copy of files once failed

	 Since AzCopy V10 does not support journal files, the task cannot resume the copy. You will have to run the task again to copy all the files.

* The log files and plan files created by AzCopy are not getting deleted after the task completes

	 The log and plan files are not deleted by the task. To explicitly clean up the files you can add a CLI step in the workflow using [this command](https://docs.microsoft.com/azure/storage/common/storage-ref-azcopy-jobs-clean).

* I'm not sure which version of AzCopy is being used in the task? I need help specifying the additional arugments accordingly

	The following are the versions of AzCopy are used in the task
	- Task version 4: AzCopy V 10. [Look here for list of arguments and their usage](https://docs.microsoft.com/azure/storage/common/storage-ref-azcopy-copy)
	- Task version 3 or below: AzCopy V 7. [Look here for list of arguments and their usage](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)


## **Recommended Documents**

* [Azure File Copy V 4](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-file-copy?view=azure-devops#faq)
* [Azure File Copy V3 or below](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-file-copy-version3?view=azure-devops)
* [AzCopy V 10](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10)
