<properties
	pageTitle="Azure virtual machines or scale sets tasks"
	description="Issues related to deployment to VMSS, nodes update or any guidance with the usage of the task"
	infoBubbleText="Azure Pipelines issues related to Azure virtual machines or scale sets tasks"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsPipelinesAzureSQLIssues"
	supportTopicIds="32742303"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Azure virtual machines or scale sets tasks

## **Recommended Steps**

Are you facing one of these common problems?

* **I'm unable to run my application in Azure pipelines which makes use of VM and VM scale sets.**
	
    This happens when your application running in the VM or VM scale sets is terminated. If you don't want the process to be closed, please  create and set a variable **Process.clean=false**. But when you create a new release next time, you need to close the server before starting it.

* **I want to deploy the application on virtual machine scale set.**

    [Follow these steps](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-deploy-app#:~:text=To%20run%20applications%20on%20virtual,scripts%20on%20existing%20VM%20instances.)

* **My Build pipeline is failing with PowerShell task on the remote machine**

    Ensure that WinRM is configured and associated on the remote machine to execute the PowerShell task. [Refer this document](https://docs.microsoft.com/azure/virtual-machines/windows/winrm)


## **Recommended Documents**

* [Deploy your application on virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-deploy-app#:~:text=To%20run%20applications%20on%20virtual,scripts%20on%20existing%20VM%20instances.)
* [Tutorial: Install applications in virtual machine scale sets with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-install-apps-powershell)
* [Tutorial: Deploy apps to virtual machine scale sets in Azure using Ansible](https://docs.microsoft.com/azure/developer/ansible/vm-scale-set-deploy-app)
* [Tutorial: Create and manage a virtual machine scale set with the Azure CLI](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-create-and-manage-cli)
* [Tutorial: Create and manage a virtual machine scale set with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-create-and-manage-powershell)