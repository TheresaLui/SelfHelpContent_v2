<properties
    pageTitle="VM boot error: Default Domain Controllers Policy"
    description="Virtual machine became unresponsive while applying the Defualt Domain Controllers Policy."
    infoBubbleText="The OS becomes hung during boot with the message 'Default Domain Controllers Policy'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-DEFAULT_DOMAIN_CONTROLLERS_POLICY"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Default Domain Controllers Policy
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because either changes were recently made to the Default Domain Controllers Policy, or due to another issue which can be determined by a memory dump analysis.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Default Domain Controllers Policy**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [VM is unresponsive while applying default domain controllers policy](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/vm-unresponsive-domain-controllers-policy) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
