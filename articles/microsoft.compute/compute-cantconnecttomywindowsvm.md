<properties
    pageTitle="Resolve connection issue with your Windows VM"
    description="Resolve connection issue with your Windows VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ram-kakani,timbasham,scottazure"
    ms.author="scotro,tibasham,ramakk"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds="32615531,32615526,32615530,32740112"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="429c106f-4adb-4ed7-a90b-b7df98686adf"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Resolve connection issue with your Windows VM
4 out of 5 customers resolved their VM connectivity issue using the steps listed below.<br>

## **Recommended Steps**

As a first step you can try to redeploy your VM in the Azure Portal.

[Redeploy VM](button-data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId)

If you cannot connect to your Windows virtual machine (VM) and are unsure of the cause, you can start by accessing the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId) for your VM and determine if the VM is experiencing a boot error.<br>

### If your VM is not at the ctrl-alt-del screen, it may be experiencing a boot error

1. Restart the virtual machine to address boot issues by clicking **Restart** at the top of the [VM resource blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId)
1. If your VM fails to start and you recently applied Windows Updates please see [Troubleshooting VM not booting after Windows Update](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-stuck-updating-boot-error)
1. Review the [common boot errors and solutions for non-bootable VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-error-troubleshoot) troubleshooting guide

### VM is at the ctrl-alt-del screen - issues external to the VM (Load Balancer, NSG, ExpressRoute)

Use [Network Watcher](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to help diagnose connectivity issues to your VM.

Try using [Azure Bastion](data-blade:Microsoft_Azure_HybridNetworking.BastionHostBlade.resourceId.$resourceId) to connect to your VM.  [Azure Bastion](https://docs.microsoft.com/azure/bastion/bastion-overview) provides secure and seamless RDP connectivity to your virtual machine directly in the Azure portal over TLS. When you connect via Azure Bastion, your virtual machine does not need a public IP address, or inbound NSG rule allowing RDP traffic.

1. [Review effective network security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId) to ensure an NSG inbound "Allow" rule exists for RDP traffic (default port 3389), and the rule is prioritized
1. Edit a [network security group rule](data-blade:microsoft_azure_compute.NetworkingBlade.id.$resourceId) that is blocking traffic
1. If you are using VPN S2S, RDP to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises.

### VM is at the ctrl-alt-del screen - issues internal to the VM

1. Resetting your VMs RDP configuration [here](data-blade:microsoft_azure_compute.VirtualMachinePasswordReset.id.$resourceId) or by following instructions in the guide: [Reset Remote Access to address RDP issues using PowerShell or CLI](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection?toc=%2Fazure%2Fvirtual-machines%2Fwindows%2Ftoc.json#fix-common-remote-desktop-errors)
1. If your VM has booted into Safe Mode, follow [VM boots into Safe Mode](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-safe-mode)
1. If you are seeing a red X over the network icon on the screenshot, follow [Cannot connect due to netvsc.sys issue](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-driver-netvsc)
1. If your network interface card (NIC) in the guest OS may be disabled or misconfigured, follow [NIC disabled in guest OS](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-nic-disabled)
1. [Verify if the guest OS firewall is misconfigured](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/guest-os-firewall-misconfigured)
1. [Disable the guest OS Firewall in Azure VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/disable-guest-os-firewall-windows)
1. [Enable or disable a firewall rule on an Azure VM Guest OS](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/enable-disable-firewall-rule-guest-os)
1. [Azure VM Guest OS firewall is blocking all inbound traffic](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/guest-os-firewall-blocking-inbound-traffic)

### If you still are encountering RDP errors

1. [Basic RDP Troubleshooting in Azure VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
1. [Troubleshooting general RDP errors in Azure VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-general-error)
1. [The Remote Desktop license server is not available when you connect via RDP to an Azure VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-no-license-server)
1. Review the [common RDP errors and solutions for Azure VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)

## **Recommended Documents**

* [Review the RDP troubleshooting guide](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)
* [Detailed troubleshooting across network components](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp)
* Access the [Serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM and verify it is running. Review the network state and system state in the [serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId) of your VM by going to command prompt.
