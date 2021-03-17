<properties
  pagetitle="Azure pipelines issues while making use of Azure virtual machines or scale sets tasks&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742303"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azvmsandscalesetsissues"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Azure virtual machines or scale sets tasks

Resolve common issues with VMs and scale sets tasks using the following steps.

## **Recommended Steps**


* My application successfully starts on VM or VMSS using Azure pipelines. However, the application process is terminated in the *Finalize Job* of the pipeline run.
	
    All processes started by Azure pipelines are terminated and cleaned up in the **Finalize Job**. If you don't want the processes to be closed, please create and set a variable **Process.clean=false**. The next time you create a new release, you'll need to close the previous application before deploying a new one.

* I want to deploy the application on virtual machine scale set.

    [Follow these instructions](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-deploy-app#:~:text=To%20run%20applications%20on%20virtual,scripts%20on%20existing%20VM%20instances)

* My Build pipeline is failing with PowerShell task on the remote machine

    Ensure that WinRM is configured and associated on the remote machine to execute the PowerShell task. [Refer to this document](https://docs.microsoft.com/azure/virtual-machines/windows/winrm).

## **Recommended Documents**

* [Deploy your application on virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-deploy-app#:~:text=To%20run%20applications%20on%20virtual,scripts%20on%20existing%20VM%20instances.)
* [Tutorial: Install applications in virtual machine scale sets with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-install-apps-powershell)
* [Tutorial: Deploy apps to virtual machine scale sets in Azure using Ansible](https://docs.microsoft.com/azure/developer/ansible/vm-scale-set-deploy-app)
* [Tutorial: Create and manage a virtual machine scale set with the Azure CLI](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-create-and-manage-cli)
* [Tutorial: Create and manage a virtual machine scale set with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-create-and-manage-powershell)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
