<properties
	pageTitle="Azure PowerShell & Azure CLI"
	description="Issues related to script execution error, modules not loaded, authentication error or any guidance with the usage of the tasks."
	infoBubbleText="Azure Pipelines issues related to script execution through both PowerShell & Azure CLI"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZPowerShellandCli"
	supportTopicIds="32742299"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Azure PowerShell & Azure CLI

## **Recommended Steps**

Are you facing one of these common problems?

* **AzCopy** failed on Hosted Agent with powershell task

    Ensure you are using the latest version of AzCopy. If an older version is used, [refer this document](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10) and  download the latest version.

* Unable to run templates and powershell scripts using Azure Cli task in YAML 

    Change the task and use [Azure PowerShell task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-powershell?view=azure-devops)

* My release pipeline PowerShell tasks gives an error "Initializing AZ module failed"

   If the module was recently installed, retry after restarting the Azure Pipelines agent. This happens when the agent doesn't have the new modules.

* Is there a way to input parameters in YAML pipelines which uses PowerShell script in it?

    Considering that a PowerShell script is being called inside the pipeline [refer this document](https://docs.microsoft.com/azure/devops/pipelines/process/runtime-parameters?view=azure-devops&tabs=script) which helps you to define and modify your variables in a PowerShell script and [call the template with the parameters defined](https://docs.microsoft.com/azure/azure-resource-manager/templates/deploy-powershell#pass-parameter-values).

* I am unable to use **Get-AzContext** inside a powershell script when using the **AzureCLI@2** task.

    The **Get-AzContext** cmdlet is part of the AZ Powershell module and is not present within the Azure Cli or the AzureCLI@2 task. If a Self-Hosted Agent is being used, this can be bypassed by having the AZ module installed on the machine where a private agent is running. Replace the **AzureCLI@2** task with the **AzurePowershell@4** task.

* I'm facing an issues with the error message **Script is not working in devops, but I'm able to run it correctly on my local machine"
   
    This usually happens when Service Principal being used might not have the same set of privileges that you have when running the same script in a shell locally. To remedy this, you must run the script locally using the same service principal details as is being used in Azure DevOps.


## **Recommended Documents**

* [Install Azure PowerShell Module](https://docs.microsoft.com/powershell/azure/install-az-ps?view=azps-4.6.1)
* [Azure PowerShell task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-powershell?view=azure-devops)
* [Use PowerShell scripts to customize the build pipelines](https://docs.microsoft.com/azure/devops/pipelines/scripts/powershell?view=azure-devops&tabs=yaml)
* [AZ Commands](https://docs.microsoft.com/cli/azure/reference-index?view=azure-cli-latest#az-login)
* [Azure CLI task](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-cli?view=azure-devops)
* [Using Command Line task in the pipelines](https://docs.microsoft.com/azure/devops/pipelines/tasks/deploy/azure-cli?view=azure-devops)
