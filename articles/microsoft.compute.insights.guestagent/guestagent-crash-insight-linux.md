<properties
	pageTitle="VM Agent Crash Insight"
    description="Resolve VM Agent Crash-Unhealthy state"
    infoBubbleText="Resolve VM Agent Crash-Unhealthy state"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS"
    ms.author="mnanda"
    displayOrder=""
    articleId="guestagent_statuscheck_linux"
    diagnosticScenario="Resolve VM Agent Crash-Unhealthy state"
    selfHelpType="diagnostics"
    supportTopicIds="32628268"
    resourceTags="linux, redhat, Ubuntu"
    productPesIds="16342,15571,15797,16454,16470"
    cloudEnvironments="public,fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Resolve VM Agent issues with your Linux VM

<!--issueDescription-->
Most customers can resolve VM Agent issues by using the following steps. If the VM Agent is in a crashed, unknown, or unhealthy state, this can impact extensions on the VM. These issues can also impact the VM Agent's ability to send Heartbeat signals for VM health.
<!--/issueDescription-->

## **Recommended Steps**

**Note**: We recommend following the troubleshooting steps to identify the problem, and then performing the remediation steps, before opening a support ticket.

For the VM **<!--$vmname-->[vmname]<!--/$vmname-->**, you can start troubleshooting VM Agent issues in the [VM overview blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/overview) and check for "Agent Status" property. If the "Agent Status" reflects an unknown or unhealthy state the below steps may help. (The "Agent Status" property will only display if the VM is running.)

### Critical VM Agent Services

The VM that is migrated to Azure from on-premises or that is created by using a customized image doesn't have Linux Guest Agent installed. In these scenarios, you have to manually install the VM agent. For more information about how to install the VM Agent, see [How to update, install Linux Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent)

The Linux agent depends on some system packages in order to function properly:

* Python 2.6+
* OpenSSL 1.0+
* OpenSSH 5.3+
* Filesystem utilities: sfdisk, fdisk, mkfs, parted
* Password tools: chpasswd, sudo
* Text processing tools: sed, grep
* Network tools: ip-route
* Kernel support for mounting UDF filesystems.


### Checked connectivity to Wireserver?

* Check whether the Azure Linux Guest Agent service is running. [More info](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/linux-azure-guest-agent#step-1-check-whether-the-azure-linux-guest-agent-service-is-running)
* Because the WireServer IP is not reachable, connect to the VM by using SSH, and then try to access the following URL from curl: http://168.63.129.16/?comp=versions
* Check for any issues that might be caused by a firewall, a proxy, or other source that could be blocking access to the IP address 168.63.129.16.
* Check whether Linux IPTables or a third-party firewall is blocking access to ports 80, 443, and 32526. For more information about why this address should not be blocked, see What is IP address 168.63.129.16.


## **Recommended Documents**

* [Linux Azure Guest Agent](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/linux-azure-guest-agent)
* [Azure Virtual Machine Agent Overview](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-linux)
* [Instal Linux VM Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent)
* [Troubleshoot VM Extensions Issues](https://docs.microsoft.com/azure/virtual-machines/extensions/features-linux)
