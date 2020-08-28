<properties
    pageTitle="VM boot error: Applying Audit Policy Configuration policy"
    description="Virtual machine becomes hung while Applying Audit Policy Configuration policy and cannot complete the boot process."
    infoBubbleText="The VM becomes unresponsive with the message: 'Applying Audit Policy Configuration policy'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-APPLYING_AUDIT_POLICY_CONFIGURATION_POLICY"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Applying Audit Policy Configuration policy
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because there are conflicting locks when the policy attempts to clean up old user profiles.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would show the message: **Applying Audit Policy Configuration policy**. This may also help you diagnose future issues and determine if a boot error is the cause.

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Virtual machine is unresponsive while applying audit policy configuration policy](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/vm-unresponsive-applying-audit-configuration-policy) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
