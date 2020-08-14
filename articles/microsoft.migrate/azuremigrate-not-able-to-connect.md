<properties
    pageTitle="Not able to connect to the VM after migration or test migration"
    description="Self help article to troubleshoot issues connecting to the virtual machine after migration"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="deseelam"
    ms.author="deseelam"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675756"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5e2a4f2f-34a4-4c04-9b07-10ca56c915bc"
	ownershipId="Compute_AzureMigrate"
/>

# Unable to connect to Azure VM post migration - Windows and Linux

## **Recommended Steps**

### Verify if your VM has booted up and is running

Use Boot diagnostics/Serial Console to validate if your VM has booted up. Boot diagnostics and Serial Console can be accessed from the left menu of the Virtual Machines page. For Boot diagnostics, you should see the VM login page. Use the Serial Console to ensure you can connect to the VM.

If your VM has booted up, but you are unable to connect to your VM, please refer to the **Unable to connect to VM** section below. If your VM has not booted up, refer to the **VM boot troubleshoot** section below.

### **Unable to connect to VM**

* Try logging into the VM using the Serial Console (SAC). You can use this [document](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-windows) (Windows) and [document](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-linux) (Linux) to turn on SAC if it’s not enabled.
* For both Windows and Linux VMs alike, use a public IP to connect to the VM if you are connecting over the internet or a private IP can work if you have a Site to Site VPN connection.

#### **Troubleshooting for Windows**

* Ensure that your VM has an IP address that can be reached over the Internet. Verify that there are no network security group (NSG) rules that are blocking RDP connections to your Azure VM. Use this [article](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nsg-problem) to troubleshoot.
* Verify if there are any firewall rules or intrusion prevention software that may be restricting RDP connections (both Azure and your on-premises firewall rules and proxy settings). Ensure that the guest OS firewall is not restricting inbound RDP traffic across firewall profiles. This [document](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/guest-os-firewall-blocking-inbound-traffic) will be helpful here.
* If you are migrating a **Windows Server 2003** VM to Azure, ensure you prepare your machine for migration. Use this [article](https://docs.microsoft.com/en-us/azure/migrate/prepare-windows-server-2003-migration) to prepare your machine for migration.
* You cannot connect remotely to **Windows Server 2016** VM or Windows 10 VMs because of netvsc.sys. You can identify this error with a red "X" on the NIC from the Boot diagnostics screenshot. This issue occurs if you are running Windows build 14393 or build 15063 on your machine. Please refer to this [documentation](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-driver-netvsc) to troubleshoot the issue.
* Ensure that the migrated machine allows remote connections. You can use the Serial Console (cmd or PowerShell) to set RDP if it is not enabled.
* A static IP should not be configured on the VM NIC. Make sure that the VM is set to use DHCP to obtain an IP address. USe this [guide](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-static-ip) to troubleshoot.
Ensure that your VM's NIC is not in a disabled state. Use this as a [guide](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nic-disabled) to help you.

#### **Troubleshooting for Linux:**

* Ensure that your VM has an IP address that can be reached over the internet. Check [security rules](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection#check-security-rules) to confirm if there are network security group (NSG) rules that are blocking SSH connections. Please ensure an inbound "Allow" NSG rule exists and is prioritized for SSH port (default 22).
* A static IP should not be configured on the VM's NIC. Make sure that the VM is set to use DHCP to obtain an IP address. If not, use the command line or edit the appropriate network configuration file for your Linux distro to make this change.
* Ensure that the migrated machine has SSH enabled and that it is configured to start automatically on boot. You can use the Serial Console to validate this. Use this [document](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection) as a guide to perform basic troubleshooting steps. Use the same document to check the port SSH is running on and to reset SSH configuration if necessary.
* Ensure that there are no firewall rules or intrusion prevention software that may be restricting the SSH connection (both Azure and your on-premises firewall rules and proxy settings).
* Make sure your ethernet or NIC ports re UP. Execute appropriate commands to bring the port UP if it was down.

### **VM boot troubleshoot**

If your VM has not booted up,

* Note: VMs with UEFI boot aren’t supported for the Agentless Migration method. Please use the [Agent-based approach](https://docs.microsoft.com/azure/migrate/tutorial-migrate-physical-virtual-machines) to perform your migration. 
* [For Linux VMs] If you are trying to migrate Linux VMs using the Agentless Migration workflow (for VMware VMs), use this [article](https://docs.microsoft.com/azure/migrate/prepare-for-migration#linux-machines) to check if your OS version would be automatically prepared for Azure. If not, please use the same [article](https://docs.microsoft.com/azure/migrate/prepare-for-migration#linux-machines) to manually prepare your VM/server for Azure. Retry the migration once you complete it.
* You can additionally review any information/details on the Server Migration jobs that were not marked successful. This may give additional insights into the failures, potential causes, and possible resolutions.
* If you are preparing the VM manually, ensure that you select the correct OS disk for migration. Choosing a Data disk instead of the OS disk can cause a VM boot error.

**Tip :** For a quick workaround to connect to your VM, you can use the Serial Console or the Portal to add a new NIC with a different IP address to your Azure VM.

If your issue persists, please raise a support ticket, and also include details about any error message you may be seeing, your VM name, and Operating System and version. [Enable the Serial Console](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-windows) to aid faster troubleshooting.

If you need to fix a configuration on the on-premises machine, wait for a while to allow the configuration change to be replicated and then retry the test migration.


## **Recommended Documents**

- [Troubleshoot RDP connection to Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)
- [Troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)
- [Detailed troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-ssh-connection) 