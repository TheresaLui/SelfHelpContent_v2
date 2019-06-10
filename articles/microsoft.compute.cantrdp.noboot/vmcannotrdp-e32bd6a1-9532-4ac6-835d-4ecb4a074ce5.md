<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because it found the OS to be unhealthy and the automatic system recovery tried to fix it."
    infoBubbleText="A boot error 'Error 0xC0000098 - STATUS FILE INVALID' has been found for your virutal machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="VMCannotRDP_14B92737-EB19-48C4-A136-D38E70C09FEC

"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM Boot Error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operation system.

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**

1. If the OS Disk is encrypted, then verify that you are in a [https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Features/Disk_Encryption/TSG/Unable_to_reach_the_key_vault_for_Standard_VM_type_machines](Unable to reach the key vault for Standard VM type machines")

    1. [Unlock an encrypted disk](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/Features/Disk_Encryption/HowTo/Unlock_an_encrypted_disk_V2) 
    2. Power the machine down and once it is stopped de-allocated to do the copy..

2. [Stop the VM and create a snapshot](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager)
3. Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/blob/master/VMRecovery/ResourceManager/New-AzureRMRescueVM.ps1)
4. If the disk is unmanaged, fix it by using [Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/?LinkId=708343)
    1. Proceed to add the Azure account details so you can access the storage accounts.
    2. Click on *Add Account Settings*, then *Add an account*.
    3. Go to the storage account where the OS disk is, you can see this on ASC under Resource Explorer on Properties in the VM Properties card.
    4. Create a snapshot of this disk by a right click over the disk and select *Make Snapshot*.
    5. Using [Azure Powershell](https://www.microsoft.com/web/handlers/webpi.ashx/getinstaller/WindowsAzurePowershellGet.3f.3f.3fnew.appids), You can follow How to [Clone a disk using Powershell](https://www.csssupportwiki.com/index.php/curated:Azure/Virtual_Machine/CantRDPSSH/HowTo/Clone_a_disk_using_PS)

5. If the disk is managed, use Azure portal to take a snapshot.
    1. Sign in to the Azure portal.
    2. Starting in the upper-left, click *New* and search for snapshot.
    3. In the Snapshot blade, click *Create*.
    4. Enter a Name for the snapshot.
    5. Select an existing Resource group or type the name for a new one.
    6. Select an Azure datacenter Location.
    7. For Source disk, select the Managed Disk to snapshot.
    8. Select the Account type to use to store the snapshot. We recommend Standard_LRS unless you need it stored on a high performing disk.
    9. Click *Create*.