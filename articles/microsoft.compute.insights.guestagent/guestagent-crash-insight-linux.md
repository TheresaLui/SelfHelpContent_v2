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

For the VM **<!--$vmname-->[vmname]<!--/$vmname-->**, you can start troubleshooting VM Agent issues in the [VM overview blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/overview) and check the `Agent Status` property. If the `Agent Status` reflects an unknown or unhealthy state, the following steps can help. (The "Agent Status" property will display only if the VM is running.)

### Critical VM Agent Services

A VM that's migrated to Azure from on-premises or that's created by using a customized image doesn't have Linux Guest Agent installed. In these scenarios, you need to manually install the VM agent. See [How to update or install Linux Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent).

To function properly, the Linux agent depends on the follow system packages:

* Python 2.6+
* OpenSSL 1.0+
* OpenSSH 5.3+
* Filesystem utilities: `sfdisk`, `fdisk`, `mkfs`, `parted`
* Password tools: `chpasswd`, `sudo`
* Text processing tools: `sed`, `grep`
* Network tools: `ip-route`
* Kernel support for mounting UDF filesystems


### Check connectivity to Wireserver

* [Check whether the Azure Linux Guest Agent service is running](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/linux-azure-guest-agent#step-1-check-whether-the-azure-linux-guest-agent-service-is-running)
* Because the WireServer IP is not reachable, connect to the VM by using SSH, and then try to access the following URL from `curl 'http://168.63.129.16/?comp=versions' `
* Check for any issues that might be caused by a firewall, a proxy, or other source that could be blocking access to the IP address 168.63.129.16.
* Check whether Linux `IPTables` or a third-party firewall is blocking access to ports 80, 443, and 32526. For more information about why this address should not be blocked, see [What is IP address 168.63.129.16?](https://docs.microsoft.com/azure/virtual-network/what-is-ip-address-168-63-129-16#:~:text=IP%20address%20168.63.129.16%20is%20a%20virtual%20public%20IP,be%20presented%20as%20a%20unique%20public%20IP%20address)

## **Recommended Documents**

* [Linux Azure Guest Agent](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/linux-azure-guest-agent)
* [Azure Virtual Machine Agent Overview](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-linux)
* [Instal Linux VM Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent)
* [Troubleshoot VM Extensions Issues](https://docs.microsoft.com/azure/virtual-machines/extensions/features-linux)
