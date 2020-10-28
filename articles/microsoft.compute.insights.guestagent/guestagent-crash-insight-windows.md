<properties
    pageTitle="VM Agent Crash Insight"
    description="Resolve VM Agent Crash-Unhealthy state"
    infoBubbleText="Resolve VM Agent Crash-Unhealthy state"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS"
    ms.author="mnanda"
    displayOrder=""
    articleId="guestagent_statuscheck_windows"
    diagnosticScenario="Resolve VM Agent Crash-Unhealthy state"
    selfHelpType="diagnostics"
    supportTopicIds="32628268"
    resourceTags="windows, windowsSQL"
    productPesIds="14749,14745,16080"
    cloudEnvironments="public,fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Resolve VM Agent issues with your Windows VM

4 out of 5 customers resolved their [VM Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows) issues using the steps listed below. The VM Agent being in a crashed, unknown, or unhealthy state can impact extensions on the VM. These issue could also impact VM Agent's capability to send Heartbeat signals for VM health.

## **Recommended Steps**

**Note**: It is recommended to follow the troubleshooting steps below to first identify the problem, then perform the remediation step(s) before opening a support ticket.

For the VM **<!--$vmname-->[vmname]<!--/$vmname-->**, you can start troubleshooting VM Agent issues in the [VM overview blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/overview) and check for "Agent Status" property. If the "Agent Status" reflects an unknown or unhealthy state the below steps may help. (The "Agent Status" property will only display if the VM is running.)

### Critical VM Agent Services
A VM that is migrated to Azure from on-premise or that is created by using a customized image doesn't have the Windows Azure VM Agent installed. In these scenarios you need to manually install the Windows Azure VM Agent. For more information about how to install the Windows Azure VM Agent, see [Azure VM Agent Overview](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows).

Following services listed below are key for VM Agent in Windows VM. These should be healthy and running:

* Windows Azure VM Agent Service
* Telemetry Service
* RD Agent service


### Check connectivity to the Wireserver?

1. Using a tool such as [PsPing](https://docs.microsoft.com/sysinternals/downloads/psping) to test whether the VM can connect to 168.63.129.16 on ports 80, 32526 and 443.
1. If the VM doesn’t connect as expected, check whether outbound communication over ports 80, 443, and 32526 are open in your local firewall on the VM.
1. If this IP address is blocked, VM Agent may display unexpected behavior in a variety of scenarios.
1. If you still cannot reach the 168.63.129.16, check the network interface to determine whether it is set as DHCP-enabled and has DNS. To check the DHCP status, of the network interface, run the 
following command: `netsh interface ip show config`.
1. If DHCP is disabled, run the following making sure you change "Interface Name" to reflect the name of the your network interface: `netsh interface ip set address name="Interface Name" source=dhcp`.

[More Info](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-azure-guest-agent)

## **Recommended Documents**

* [More Info](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-azure-guest-agent)
* [Azure Virtual Machine Agent Overview](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows)
* [Instal VM Agent in Offline Model ](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/install-vm-agent-offline)
* [Troubleshoot VM Extensions Issues](https://docs.microsoft.com/azure/virtual-machines/extensions/troubleshoot)
