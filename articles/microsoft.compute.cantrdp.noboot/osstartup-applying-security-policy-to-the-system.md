<properties
    pageTitle="VM boot error: Applying Security Policy to the System"
    description="Virtual machine becomes unresponsive while it applies a security policy to the system."
    infoBubbleText="The VM becomes stuck while dsiplaying 'Applying security policy to the system'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-APPLYING_SECURITY_POLICY_TO_THE_SYSTEM"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Applying Security Policy to the System
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state due to many potential causes. To determine the root cause, a memory dump analysis will need to be performed.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Applying Security Policy to the System**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [VM is unresponsive while applying Security Policy to the system](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/unresponsive-vm-apply-security-policy) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
