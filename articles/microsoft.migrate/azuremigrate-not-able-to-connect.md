<properties
    pageTitle="Not able to connect to the VM after migration/test migration"
    description="Self help article to troubleshoot issues connecting to the virtual machine after migration"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="bsiva"
    ms.author="bsiva"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675756"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5e2a4f2f-34a4-4c04-9b07-10ca56c915bc"
	ownershipId="Compute_AzureMigrate"
/>

# Not able to connect to the Azure VM after migration

## **Recommended Steps**

- Ensure that the on-premises machine allows remote connections
- For Linux machines, ensure that the on-premises (the actual machine being migrated) machine has SSH enabled and that it is configured to start automatically on boot
- For Windows machines, ensure that the on-premises (the actual machine being migrated) machine has Remote Desktop enabled and that remote desktop connections are allowed by the Windows Firewall

    If you need to fix a configuration on the on-premises machine, wait for a while to allow the configuration change to be replicated and then retry the test migration.

- Ensure that there are no network security group rules that are blocking connections to the test virtual machine in Azure
- Ensure the VM has booted up and is running. To do this by use Boot diagnostics for Windows virtual machines, and use the Azure Serial console for Linux virtual machines. To view boot diagnostics, go to the virtual machines > Select the VM > Select boot diagnostics from the VM menu. For Windows VMs you should see the Windows splash screen. For Linux VMs use the serial console from the VM menu to ensure you are able to connect to the VM.

### Cannot connect to Windows 10 or Windows Server 2016 VM in Azure because of netvsc.sys

- Typically this issue occurs with Windows build 14393 and build 15063. Please refer to this documentation to troubleshoot the issue: [How to] [troubleshoot RDP](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-driver-netvsc)

## **Recommended Documents**

- [Troubleshoot RDP connection to Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)
- [Troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)

