<properties
  pagetitle="Azure Pipelines issues related to Azure File Copy task"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="ninallam,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742296"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesazurefilecopyissues"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines issues related to Azure File Copy task

Resolve most common issues using the following solutions.

## **Recommended Steps**

* Can I run the task on a Linux Agent?<br>
  This task is written in PowerShell and therefore works only when run on Windows agents. If your pipelines require Linux agents and need to copy files to an Azure Storage Account, consider running az storage blob commands in the [Azure CLI task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-cli?view=azure-devops) as an alternative.

* The task is failing due to authentication issues<br>
  If you use task version 4, the Service Principal will require more permissions for enhanced security. The following permissions must be provided:<br>
  - [Storage Blob Data Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor)<br>
  - [Storage Blob Data Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-data-owner)<br>
  For more details on the level of authorization [look here](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10#option-1-use-azure-active-directory)

* The task is not resuming copy of files after it fails<br>
  Since AzCopy V10 does not support journal files, the task cannot resume the copy. Run the task again to copy all the files.

* The log files and plan files created by AzCopy are not getting deleted after the task completes<br>
  The log and plan files are not deleted by the task. To explicitly clean up the files you can add a CLI step in the workflow using [this command](https://docs.microsoft.com/azure/storage/common/storage-ref-azcopy-jobs-clean).

* I'm not sure which version of AzCopy is being used in the task? I need help specifying the additional arguments accordingly<br>
  The following are the versions of AzCopy are used in the task:<br>
  - Task version 4: AzCopy V10. [Look here for list of arguments and their usage](https://docs.microsoft.com/azure/storage/common/storage-ref-azcopy-copy)<br>
  - Task version 3 or below: AzCopy V7. [Look here for list of arguments and their usage](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)


## **Recommended Documents**

* [Azure File Copy V4](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-file-copy?view=azure-devops#faq)
* [Azure File Copy V3 or below](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-file-copy-version3?view=azure-devops)
* [AzCopy V10](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
