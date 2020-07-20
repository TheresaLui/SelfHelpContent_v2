<properties
    pageTitle="VM boot error: Applying Group Policy Local Users and Groups policy"
    description="Virtual machine becomes hung while Applying Group Policy Local Users and Groups policy and cannot complete the boot process."
    infoBubbleText="The VM becomes unresponsive with the message: 'Applying Group Policy Local Users and Groups policy'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-APPLYING_GROUP_POLICY_LOCAL_USERS_AND_GROUPS_POLICY"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax"
    ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Applying Group Policy Local Users and Groups policy
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because there are conflicting locks when the policy attempts to clean up old user profiles.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would show the message: **Applying Group Policy Local Users and Groups policy**. This may also help you diagnose future issues and determine if a boot error is the cause.

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Applying Group Policy Local Users and Groups policy](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/unresponsive-vm-apply-group-policy) troubleshooting guide

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
