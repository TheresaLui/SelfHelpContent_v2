<properties  
    pageTitle="I need to reset my password"
    description="I need to reset my password"
    service=""
    resource=""
    authors="ScottAzure"
    ms.author="scotro"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615529"
    resourceTags=""
    productPesIds="15571,15797,16454,16470,16342"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="28c55293-b977-4d19-b98c-338f450a6aa4"
	ownershipId="Compute_VirtualMachines"
/>

# I need to reset my password

4 out of 5 customers resolved their VM reset password issue using the steps below.<br>

## **Recommended Steps**

If you can't connect to a Linux virtual machine (VM) and you think you can resolve the issue by resetting the SSH service configuration, by restarting, or by resetting a local user's password, you can perform those actions using Password Reset Blade in the Azure Portal or VM Access extension using Azure CLI.<br>

[Reset VM Password](button-data-blade:microsoft_azure_compute.VirtualMachinePasswordReset.id.$resourceId)

If you're using Azure CLI, make sure that you have the latest [latest CLI module installed](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) and configured and that you're signed in to your Azure subscription. You can also [perform these steps for VMs created with the classic deployment model](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#vms-created-by-using-the-classic-deployment-model).

You can **reset or restart the SSH Service** and **reset credentials** in the following ways:<br>

1. Read the online documentation:<br>

  * [Reset SSH credentials for a user](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#reset-ssh-credentials-for-a-user)<br>
  * [Reset SSH configuration and restart SSH service](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#reset-the-ssh-configuration)<br>
  * [Update SSH key](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#use-the-azure-portal)

2. Connect to the Azure portal and **[perform the reset actions using the Password Reset Blade](data-blade:Microsoft_Azure_Compute.VirtualMachinePasswordReset.id.$resourceId)**<br>
3. Alternatively, [perform the reset actions using CLI and VMAccess extension for Linux](https://docs.microsoft.com/azure/virtual-machines/extensions/vmaccess#ways-to-use-the-vmaccess-extension)

If the preceding steps don't work, you can also use the offline method of [resetting the password by attaching the source OS virtual disk to another VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-password). Only use this process as a last resort. **Always try to reset a password using the Azure portal or Azure CLI first.**

**Note:** If you use the VMAccess Extension to reset the password of your VM after installing the AAD Login Extension, you'll need to rerun the AAD Login Extension to re-enable AAD Login for your machine.

## **Recommended Documents**

* [Using the Azure Portal to troubleshoot SSH connection issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#use-the-azure-portal)<br>
* [Troubleshoot SSH connections to an Azure Linux VM that fails, errors out, or is refused](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection)<br>
* [How to reset local Linux password on Azure VMs - Offline reset](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-password)
