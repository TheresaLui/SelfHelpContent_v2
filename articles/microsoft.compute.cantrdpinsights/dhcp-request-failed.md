<properties
    pageTitle="DHCP request failed"
    description="The DHCP request failed leaving the Guest OS of the VM without connectivity"
    infoBubbleText="The DHCP request failed leaving the Guest OS of the VM without connectivity"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    authorAlias="tibasham"
    displayOrder=""
    articleId="DHCPRequest"
    diagnosticScenario="DHCP request failed"
    selfHelpType="diagnostics"
    supportTopicIds="32615525"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# The DHCP request failed causing the VM to lose connectivity
<!--issueDescription-->
We have investigated and detected that the virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> currently does not appear to have connectivity.  This is due to a failure in the dynamic host configuration protocol (DHCP) request.
<!--/issueDescription-->

## **Recommended Steps**

* Redploy to a new host by accessing the [VM properties blade](data-blade:Microsoft_Azure_Compute.VirtualMachineProtoBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/overview) in the Azure portal and clicking `Redeploy`.<br>
* Resetting the guest NIC may restore RDP connectivity to the VM, please find instructions for mitigating this issue [here](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-network-interface).<br>
* Check that the DHCP client service is enabled, please find instructions for mitigating this issue [here](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/troubleshoot-rdp-dhcp-disabled).
