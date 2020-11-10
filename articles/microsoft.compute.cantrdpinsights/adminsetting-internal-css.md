<properties
pageTitle="Admin Account Disabled"
description="Administrator Setting"
infoBubbleText="Built-in Administrator account is disabled"
service="microsoft.compute"
resource="virtualmachines"
authors="manavis"
displayOrder=""
articleId="vmhealthsignal_2fd10e1f-f50f-4087-8269-ae7bbfb34489"
diagnosticScenario="Administrator Setting"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Built-in Administrator account is disabled
<!--issueDescription-->
We have investigated and detected that the built-in administrator account has been disabled which may prevent your connectivity to the VM via RDP.

Typically this issue has been seen in the VMs migrated from on-premises or have been created from specialized images.
<!--/issueDescription-->

## **Recommended Steps**
* Re-enabling the built-in admin account may restore your RDP connectivity to the VM.
* In order to enable the built-in admin account, please run the below script on the VM via [Custom Script Extension](https://docs.microsoft.com/azure/virtual-machines/windows/extensions-customscript):

 ```
$adminAccount = Get-WmiObject Win32_UserAccount -filter "LocalAccount=True" | ? {$_.SID -Like "S-1-5-21-*-500"}
if($adminAccount.Disabled)
{
    $adminAccount.Disabled = $false
    $adminAccount.Put()
}
 ```
