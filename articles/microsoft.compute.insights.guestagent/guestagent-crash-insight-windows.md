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

<!--issueDescription-->
Most customers can resolve VM Agent issues by using the following steps. If the VM Agent is in a crashed, unknown, or unhealthy state, this can impact extensions on the VM. These issues can also impact the VM Agent's ability to send Heartbeat signals for VM health.
<!--/issueDescription-->

## **Recommended Steps**

**Note**: We recommend following the troubleshooting steps to identify the problem, and then performing the remediation steps, before opening a support ticket.

For the VM **<!--$vmname-->[vmname]<!--/$vmname-->**, you can start troubleshooting VM Agent issues in the [VM overview blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/overview) and check for "Agent Status" property. If the "Agent Status" reflects an unknown or unhealthy state the below steps may help. (The "Agent Status" property will only display if the VM is running.)

### Critical VM Agent Services
A VM that is migrated to Azure from on-premise or that is created by using a customized image doesn't have the Windows Azure VM Agent installed. In these scenarios, you need to manually install the Windows Azure VM Agent. For more information about how to install the Windows Azure VM Agent, see [Azure VM Agent Overview](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows).

Following services listed below are important for VM Agent in Windows VM. These should be healthy and running:
* Windows Azure VM Agent Service
* Telemetry Service
* RD Agent service

### Check connectivity to the Wireserver?

1. Use a tool such as [PsPing](https://docs.microsoft.com/sysinternals/downloads/psping) to test whether the VM can connect to 168.63.129.16 on ports 80, 32526, and 443.
1. If the VM doesn’t connect as expected, check whether outbound communication over ports 80, 443, and 32526 are open in your local firewall on the VM.
1. If this IP address is blocked, VM Agent may display unexpected behavior in a variety of scenarios.
1. If you still can't reach the 168.63.129.16, check the network interface to determine whether it is set as DHCP-enabled and has DNS. To check the DHCP status, of the network interface, run the 
following command: `netsh interface ip show config`.
1. If DHCP is disabled, run the following command, making sure that you change "Interface Name" to reflect the name of the your network interface: `netsh interface ip set address name="Interface Name" source=dhcp`.

Learn more about [troubleshooting Windows Azure Guest Agent](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/windows-azure-guest-agent)

## **Recommended Documents**

* [Azure Virtual Machine Agent Overview](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows)
* [Instal VM Agent in Offline Model ](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/install-vm-agent-offline)
* [Troubleshoot VM Extensions Issues](https://docs.microsoft.com/azure/virtual-machines/extensions/troubleshoot)
