<properties
    pageTitle="Azure Stack cannot connect to Linux VM"
    description="Azure Stack cannot connect to Linux VM"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663889"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6f641910-1001-4135-b8d1-85ab25fa1503"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Linux VM connectivity issues

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

**I have an issue with my public IP**

Network Security Group by default deny connections from Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps.

- Review effective security group rules to make sure that the inbound "Allow" NSG rule exists and is prioritized for SSH port (default 22)
- [Edit the Network Security Group](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group) to make changes to the rules if needed
- If there is no rule to allow the traffic from Internet, add a new rule to allow access to the backend port, with source being 'Internet', '*' or a specific public IP address

**My VM is not booting**

- [Understanding FSTAB errors and mitigation steps](https://support.microsoft.com/help/3206699/azure-linux-vm-cannot-start-because-of-fstab-errors)
- [Resolve boot errors when starting your VM after applying specific kernel changes](https://support.microsoft.com/help/4091524/how-recovery-azure-linux-vm-from-kernel-related-boot-related-issues)
- [How to use boot diagnostics to  troubleshoot Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics)

**I need to reset login password**

You can reset or restart the SSH Service and reset credentials by using one of the following methods:
- Connect to the Azure portal, and use [Reset password feature](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#use-the-azure-portal) to reset the SSH configuration and the credentials for the user
- Alternatively, [perform the reset actions using CLI](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#use-the-azure-cli) and VMAccess extension for Linux
- If **Reset password** is broken because the VMAccess extension isn't working, use a [Linux recovery VM to reset the password](https://docs.microsoft.com/azure-stack/operator/azure-stack-troubleshooting#troubleshoot-virtual-machines-vms)  
- If the above options fail, you can also use the [offline method of resetting the password by attaching the source OS virtual disk to another VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-password). Only use this process as a last resort. Always try to reset a password using the Azure portal or Azure CLI first.

Note: If you use the VMAccess Extension to reset the password of your VM after installing the AAD Login Extension, you will need to rerun the AAD Login Extension to re-enable AAD Login for your machine. 

## **Recommended Documents**

- [Troubleshoot SSH connections to an Azure Linux VM that fails, errors out, or is refused](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection)
- [Detailed SSH troubleshooting steps for issues connecting to a Linux VM in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)
- [How to use boot diagnostics to troubleshoot Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics)
- [Troubleshooting connectivity problems between Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)
- [Troubleshoot application connectivity issues on virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-app-connection)
