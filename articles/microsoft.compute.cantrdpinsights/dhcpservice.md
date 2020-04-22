<properties
    pageTitle="Windows DHCP client service is not running"
    description="The Windows DHCP client service is not running, this is impacting RDP connectivity to the VM"
    infoBubbleText="The Windows DHCP client service is not running, this is impacting RDP connectivity to the VM."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="DHCPService"
    diagnosticScenario="DHCPService"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	  ownershipId="Compute_VirtualMachines_Content"
/>

# DHCP client service is not running in the VM
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the DHCP client service is not running.
<!--/issueDescription-->

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Cannot RDP to Azure Virtual Machines because the DHCP Client service is disabled](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-dhcp-disabled) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot Remote Desktop connections to an Azure virtual machine](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
