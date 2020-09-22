<properties
    pageTitle="DHCP request failed"
    description="The DHCP request failed leaving the Guest OS of the VM without connectivity"
    infoBubbleText="The DHCP request failed leaving the Guest OS of the VM without connectivity"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="DHCPRequest"
    diagnosticScenario="DHCP request failed"
    selfHelpType="diagnostics"
    supportTopicIds="32615525"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# The DHCP request failed causing the VM to lose connectivity
<!--issueDescription-->
We have investigated and detected that the virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> currently does not appear to have connectivity. This is due to a failure in the dynamic host configuration protocol (DHCP) request.
<!--/issueDescription-->

## **Recommended Steps**

Try each of the following steps in order to resolve the issue.

1. Redeploy to a new host by accessing the [VM properties blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/overview) in the Azure portal and clicking `Redeploy`
1. [Resetting the guest NIC](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-network-interface) may restore RDP connectivity to the VM
1. Check that the [DHCP client service is enabled](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-dhcp-disabled)
