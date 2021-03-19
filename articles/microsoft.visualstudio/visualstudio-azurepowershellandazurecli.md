<properties
  pagetitle="Azure pipelines issues while making use of Azure PowerShell &amp; Azure CLI"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742299"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azpowershellandcli"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Azure PowerShell & Azure CLI

## **Recommended Steps**

* **AzCopy** failed on Hosted Agent with PowerShell task

    Ensure you are using the latest version of AzCopy. If you're using an older version, see [Storage use with AZCopy v10](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10) and  download the latest version.

* Unable to run templates and PowerShell scripts using Azure Cli task in YAML 

    Change the task and use [Azure PowerShell task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-powershell?view=azure-devops)

* My release pipeline PowerShell task gives an error **Initializing AZ module failed**

   If the module was recently installed, retry after restarting the Azure Pipelines agent. This happens when the agent doesn't have the new modules.

* Is there a way to input parameters in YAML pipelines which uses PowerShell script in it?

    Considering that a PowerShell script is being called inside the pipeline, see [this documentation](https://docs.microsoft.com/azure/devops/pipelines/process/runtime-parameters?view=azure-devops&tabs=script), which can help you to define and modify your variables in a PowerShell script and [call the template with the parameters defined](https://docs.microsoft.com/azure/azure-resource-manager/templates/deploy-powershell#pass-parameter-values).

* I am unable to use the `Get-AzContext` cmdlet inside a PowerShell script when using the **AzureCLI@2** task

    The `Get-AzContext` cmdlet is part of the AZ PowerShell module and is not present within the Azure CLI or the AzureCLI@2 task. If a Self-Hosted Agent is being used, you can bypass this issue by having the AZ module installed on the machine where a private agent is running. Replace the **AzureCLI@2** task with the **AzurePowershell@4** task.

* I'm facing an issues with the error message, "Script is not working," in Azure DevOps, but I'm able to run it correctly on my local machine
   
    This usually happens when the Service Principal being used doesn't have the same set of privileges that you have when running the same script in a shell locally. To fix  this, run the script locally using the same service principal details that are being used in Azure DevOps.

## **Recommended Documents**

* [Install Azure PowerShell Module](https://docs.microsoft.com/powershell/azure/install-az-ps?view=azps-4.6.1)
* [Azure PowerShell task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-powershell?view=azure-devops)
* [Use PowerShell scripts to customize the build pipelines](https://docs.microsoft.com/azure/devops/pipelines/scripts/powershell?view=azure-devops&tabs=yaml)
* [AZ Commands](https://docs.microsoft.com/cli/azure/reference-index?view=azure-cli-latest#az-login)
* [Azure CLI task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-cli?view=azure-devops)
* [Using Command Line task in the pipelines](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-cli?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
