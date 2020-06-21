<properties
    pageTitle="VM boot error: Out-of-Box-Experience SQL"
    description="Virtual machine failed to boot due to the Windows Boot Manager menu"
    infoBubbleText="A Windows Boot Manager prompt 'Choose an operating system to start, or press TAB to select a tool:'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-OOBE_SQL"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Out-of-Box-Experience SQL
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the image has Windows SQL 2016 installed, but wasn't prepared properly. There are some extra considerations needed when you SYSPREP a Windows image that has Windows SQL 2016 installed.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would get the error **Windows Setup could not configure Windows to run on this computer's hardware** while on the **Getting ready** screen. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

* If the image for the Virtual Machine has Windows SQL 2016 installed, then it is missing a prerequisite requirement. Follow the steps in the [Install SQL Server with SysPrep](https://docs.microsoft.com/sql/database-engine/install-windows/install-sql-server-using-sysprep?redirectedfrom=MSDN&view=sql-server-ver15) guide.

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
